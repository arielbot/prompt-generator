<template>
  <div>
    <main class="bg-white max-w-lg mx-auto p-8 md:p-12 my-10 rounded-lg shadow-2xl">
      <h2 class="block text-gray-700 text-sm font-bold mb-2 uppercase">Read a book that...</h2>
      <section>
        <div class="flex flex-col">
          <div class="pt-3 rounded bg-gray-200">
            <div class="bg-gray-200 rounded w-full text-gray-700 focus:outline-none border-b-4 border-gray-300 focus:border-purple-600 transition duration-500 px-3 pb-3 text-center">
              <p>{{ prompts[promptIndex].string }}</p>
            </div>
          </div>
          <button class="mt-6 bg-pink-400 hover:bg-pink-500 text-white font-bold py-2 rounded shadow-lg hover:shadow-xl transition duration-200" type="submit" v-on:click="randomize">Prompt Me</button>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
import readingPrompts from '~/static/data/prompts.json'

export default {
  name: 'Home',
  data() {
    return {
      prompts: readingPrompts,
      promptIndex: 0 
    };
  },
  methods: {
    randomize: function() {
      this.promptIndex = Math.floor(Math.random() * (this.prompts.length));
    }
  }
}
</script>
