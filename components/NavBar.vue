<template>
  <nav class="flex items-center justify-between flex-wrap bg-teal-500 p-6">
    <div class="flex items-center flex-shrink-0 text-white mr-6">
      <img class="navbar-logo" src="/images/book_prompts.png" alt="Bookish Prompt" />
    </div>
    <div class="block lg:hidden">
      <button class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white" @click="show = !show">
        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
      </button>
    </div>
    <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto" :class="show ? 'flex' : 'hidden'">
      <div class="text-sm lg:flex-grow">
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-white border-b-2 border-transparent hover:border-white mr-4">
          Romance
        </a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-white border-b-2 border-transparent hover:border-white mr-4">
          Fantasy
        </a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-white border-b-2 border-transparent hover:border-white mr-4">
          Randomize
        </a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-white border-b-2 border-transparent hover:border-white">
          Make Your Own
        </a>
      </div>
      <!--/* <div>
        <a href="#" class="inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-teal-500 hover:bg-white mt-4 lg:mt-0">Download</a>
      </div> */-->
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      show: false
    }
  }
}
</script>

<style>
.navbar-logo {
  width: 180px;
}
</style>