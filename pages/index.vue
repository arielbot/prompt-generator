<template>
  <div>
    <header class="max-w-lg mx-auto">
      <h1 class="text-4xl font-bold text-white text-center">Reading Prompt Generator
      </h1>
    </header>
    <main class="bg-white max-w-lg mx-auto p-8 md:p-12 my-10 rounded-lg shadow-2xl">
      <section>
            <form class="flex flex-col" method="POST" action="#">
                <button class="bg-pink-400 hover:bg-pink-500 text-white font-bold py-2 rounded shadow-lg hover:shadow-xl transition duration-200 mb-6" type="submit">Prompt Me</button>
                <div class="pt-3 rounded bg-gray-200">
                  <div class="bg-gray-200 rounded w-full text-gray-700 focus:outline-none border-b-4 border-gray-300 focus:border-purple-600 transition duration-500 px-3 pb-3 text-center">
                    prompt prints here
                  </div>
                </div>
            </form>
        </section>
        <div class="reading-prompts">
          <!-- {{ readingPrompts }} -->
        </div>
    </main>
  </div>
</template>

<script>
import readingPrompts from '~/static/data/prompts.json'
export default {
  name: 'Home',
  // async asyncData({ $axios }) {
  //   const data = await $axios.$get('/data/prompts.json')
  //   return { data }
  // }
  async asyncData({ params }) {
    return { readingPrompts }
  }
}
</script>
