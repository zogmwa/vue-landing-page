<template>
  <div class="flex flex-wrap justify-center overflow-x-auto">
    <div class="flex container mx-auto justify-center">
      <v-dropdown placement="left">
        <!-- Button content -->
        <template v-slot:button>
          <span class="px-2 py-2 rounded inline-flex items-center text-sm">
            <span class="mr-2 hover:border-b-2 border-sky-500">Overview</span>

            <svg class="w-4 h-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
              <path d="M4.516 7.548c.436-.446 1.043-.481 1.576 0L10 11.295l3.908-3.747c.533-.481 1.141-.446 1.574 0 .436.445.408 1.197 0 1.615-.406.418-4.695 4.502-4.695 4.502a1.095 1.095 0 0 1-1.576 0S4.924 9.581 4.516 9.163c-.409-.418-.436-1.17 0-1.615z" />
            </svg>
          </span>
        </template>

        <!-- Opened dropdown content -->
        <template v-slot:content>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Overview item1</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Overview item2</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Overview item3</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Overview item4</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Overview item5</a>
        </template>
      </v-dropdown>
      <v-dropdown placement="left">
        <!-- Button content -->
        <template v-slot:button>
          <span class="px-2 py-2 rounded inline-flex items-center text-sm">
            <span class="mr-2 hover:border-b-2 border-sky-500">Media</span>

            <svg class="w-4 h-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
              <path d="M4.516 7.548c.436-.446 1.043-.481 1.576 0L10 11.295l3.908-3.747c.533-.481 1.141-.446 1.574 0 .436.445.408 1.197 0 1.615-.406.418-4.695 4.502-4.695 4.502a1.095 1.095 0 0 1-1.576 0S4.924 9.581 4.516 9.163c-.409-.418-.436-1.17 0-1.615z" />
            </svg>
          </span>
        </template>

        <!-- Opened dropdown content -->
        <template v-slot:content>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Media item1</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Media item2</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Media item3</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Media item4</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Media item5</a>
        </template>
      </v-dropdown>
      <v-dropdown placement="left">
        <!-- Button content -->
        <template v-slot:button>
          <span class="px-2 py-2 rounded inline-flex items-center text-sm">
            <span class="mr-2 hover:border-b-2 border-sky-500">Fandom</span>

            <svg class="w-4 h-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
              <path d="M4.516 7.548c.436-.446 1.043-.481 1.576 0L10 11.295l3.908-3.747c.533-.481 1.141-.446 1.574 0 .436.445.408 1.197 0 1.615-.406.418-4.695 4.502-4.695 4.502a1.095 1.095 0 0 1-1.576 0S4.924 9.581 4.516 9.163c-.409-.418-.436-1.17 0-1.615z" />
            </svg>
          </span>
        </template>

        <!-- Opened dropdown content -->
        <template v-slot:content>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Fandom item1</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Fandom item2</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Fandom item3</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Fandom item4</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Fandom item5</a>
        </template>
      </v-dropdown>
      <v-dropdown placement="left">
        <!-- Button content -->
        <template v-slot:button>
          <span class="px-2 py-2 rounded inline-flex items-center text-sm">
            <span class="mr-2 hover:border-b-2 border-sky-500">Share</span>

            <svg class="w-4 h-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
              <path d="M4.516 7.548c.436-.446 1.043-.481 1.576 0L10 11.295l3.908-3.747c.533-.481 1.141-.446 1.574 0 .436.445.408 1.197 0 1.615-.406.418-4.695 4.502-4.695 4.502a1.095 1.095 0 0 1-1.576 0S4.924 9.581 4.516 9.163c-.409-.418-.436-1.17 0-1.615z" />
            </svg>
          </span>
        </template>

        <!-- Opened dropdown content -->
        <template v-slot:content>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Share item1</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Share item2</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Share item3</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Share item4</a>
          <a class="flex w-full justify-between items-center rounded px-2 py-1 my-1 hover:bg-indigo-600 hover:text-white" href="#">Share item5</a>
        </template>
      </v-dropdown>
    </div>
  </div>
</template>

<script>
  import vDropdown from "./dropdown/v-dropdown.vue"

  export default {
    components:{
      vDropdown: vDropdown
    }
  }
</script>