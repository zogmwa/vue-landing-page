<template>
  <div class="md:bg-[url('./assets/background.jpg')] mt-3">
    <div class="w-100 bg-blue-900/80">
      <div class="flex flex-col md:flex-row container mx-auto">
        <div class="flex-none flex flex-col w-[300px] my-6 mx-auto md:mx-6">
          <img class="rounded-md" :src="results?.Poster" alt="item image" />
          <div class="hidden md:flex flex-col mt-2 mx-auto">
            <span class="text-slate-300 text-left">Now Streaming</span>
            <span class="text-white font-semibold text-left">Watch Now</span>
          </div>
        </div>
        <div class="grow flex flex-col mx-8 mb-6 md:mt-6 md:ml-6">
          <span class="text-[1.2rem] md:text-[2rem] text-white font-bold text-left md:mt-4">
            {{ results?.Title ?? '' }} <span class="text-gray-400">({{ results?.Year ?? '' }})</span>
          </span>
          <div class="flex flex-col-reverse md:flex-col">
            <div class="flex flex-col md:flex-row justify-start items-center bg-slate-700 border-y border-slate-900 md:bg-slate-900/0 md:border-none py-2 -mx-8 mt-2 text-center md:mx-0 md:mt-0">
              <div class="flex items-center">
                <span class="text-gray-400 border-gray-400 rounded-md border p-1">{{ results?.Rated }}</span>
                <div class="flex">
                  <span class="text-white ml-2">{{ results?.DVD }}</span>
                  <span class="text-white mx-1">*</span>
                  <span class="text-white flex md:hidden">{{ results?.Runtime }}</span>
                </div>
              </div>
              <span class="text-white ml-2">{{ results?.Genre }}</span>
              <span class="hidden md:flex text-white mx-1">*</span>
              <span class="hidden md:flex text-white">{{ results?.Runtime }}</span>
            </div>
            <div class="flex items-center my-4">
              <div class="flex items-start p-2 border border-gray-500 rounded-full bg-slate-900/40">
                <span class="text-white text-[1.5rem] font-semibold">{{ Number(results?.imdbRating ?? 0) * 10 }}</span>
                <span class="text-gray-400">%</span>
              </div>
              <div class="flex flex-col items-start ml-2">
                <span class="text-white font-semibold">User</span>
                <span class="text-white font-semibold">Score</span>
              </div>
              <div class="hidden md:flex">
                <span class="text-white items-center mx-4">List</span>
                <span class="text-white items-center mx-4">Share</span>
                <span class="text-white items-center mx-4">Bookmark</span>
                <span class="text-white items-center mx-4">Like</span>
              </div>
              <div class="border-l border-white md:border-none ml-2 md:ml-0">
                <span class="text-white mx-2">></span>
                <span class="text-white">Play Trailer</span>
              </div>
            </div>
          </div>
          <div class="flex flex-col mt-6">
            <span class="text-left text-slate-400 italic">Obviously.</span>
            <span class="text-left mt-1 text-white text-lg font-semibold">Overview</span>
            <span class="text-left text-slate-300">{{ results?.Plot }}</span>
            <div class="grid grid-cols-2 md:grid-cols-3 mt-4 gap-4 gap-y-8">
              <div v-for="director in directors" :key="director" class="flex flex-col">
                <span class="font-bold text-white text-left">{{ director }}</span>
                <span class="text-slate-300 text-left">Director</span>
              </div>
              <div v-for="writer in writers" :key="writer" class="flex flex-col">
                <span class="font-bold text-white text-left">{{ writer }}</span>
                <span class="text-slate-300 text-left">Characters</span>
              </div>
              <div v-for="actor in actors" :key="actor" class="flex flex-col">
                <span class="font-bold text-white text-left">{{ actor }}</span>
                <span class="text-slate-300 text-left">Characters</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="flex md:hidden flex-col fixed bottom-0 w-full bg-blue-800/60">
        <div class="flex flex-col mt-2 mx-auto">
          <span class="text-slate-300 text-left">Now Streaming</span>
          <span class="text-white font-semibold text-left">Watch Now</span>
        </div>
        <div class="flex mx-auto mt-2">
          <span class="text-white items-center mx-4">List</span>
          <span class="text-white items-center mx-4">Share</span>
          <span class="text-white items-center mx-4">Bookmark</span>
          <span class="text-white items-center mx-4">Like</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      results: {},
      isLoading: false,
      error: null,
      directors: [],
      writers: [],
      actors: []
    };
  },
  methods: {
    loadExperiences() {
      this.isLoading = true;
      this.error = null;
      fetch('http://www.omdbapi.com/?i=tt3896198&apikey=d2132124')
        .then((response) => {
          if (response.ok) {
            return response.json();
          }
        })
        .then((data) => {
          this.isLoading = false;
          this.directors = data.Director.split(', ');
          this.writers = data.Writer.split(', ');
          this.actors = data.Actors.split(', ');
          this.results = data;
        })
        .catch((error) => {
          console.log(error);
          this.isLoading = false;
          this.error = 'Failed to fetch data - please try again later.';
        });
    },
  },
  created() {
    this.loadExperiences();
  },
};

</script>

