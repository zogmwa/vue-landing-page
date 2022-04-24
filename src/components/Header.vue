<template>
  <nav class="relative flex flex-wrap items-center justify-between px-2 py-3 bg-neutral-500 mb-3">
    <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
      <div class="w-full relative flex justify-between lg:w-auto  px-4 lg:static lg:block lg:justify-start">
        <button class="text-white cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none" type="button" v-on:click="toggleNavbar()">
          <span class="text-xs">Menu</span>
        </button>
        <div class="flex align-items-center">
          <a class="flex items-center justify-center" href="/">
            <img :src="pageLogo" alt="logo" class="hidden md:flex md:w-[150px]" />
            <span class="flex md:hidden text-white">Mobile logo</span>
          </a>
          <a class="hidden md:flex px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75" href="#movies">
            <span class="ml-2">Movies</span>
          </a>
          <a class="hidden md:flex px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75" href="#tv-shows">
            <span class="ml-2">TV Shows</span>
          </a>
          <a class="hidden md:flex px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75" href="#people">
            <span class="ml-2">People</span>
          </a>
        </div>
        <button class="text-white cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none">
          <span class="text-xs">Man</span>
        </button>
      </div>
      <div v-bind:class="{'hidden': !showMenu, 'flex': showMenu}" class="lg:flex lg:flex-grow items-center">
        <ul class="flex flex-col lg:flex-row list-none ml-auto">
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75" href="#login">
              <span class="ml-2">Login</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75" href="#join-tmdb">
              <span class="ml-2">Join TMDB</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75" href="#search">
              <span class="ml-2">Search</span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
import pageLogo from "../assets/page-logo.svg";

export default {
  name: "neutral-navbar",
  data() {
    return {
      pageLogo,
      showMenu: false
    }
  },
  methods: {
    toggleNavbar: function(){
      this.showMenu = !this.showMenu;
    }
  }
}
</script>