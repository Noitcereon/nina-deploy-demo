<script setup lang="ts">
import { onMounted } from "vue";
import { initTheme } from "../composables/theme";
import MainLayout from "../components/MainLayout.vue";

onMounted(() => {
  initTheme();
});
</script>

<template>
  <MainLayout currentPage="Home">
    <template #default>
      <h1
        class="pb-4 text-6xl text-center text-gray-700 dark:text-gray-100 transition-colors"
      >
        Home
      </h1>
      <p class="text-gray-600 dark:text-pink-900">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde enim ipsum
        quo voluptates eos id ex saepe exercitationem necessitatibus? Dolore
        fuga quasi vel corporis illum, velit aspernatur est ex explicabo?
      </p>
      <section class="grid lg:grid-cols-3 w-full mt-6 gap-3">
        <div class="flex justify-center bg-pink-200 dark:bg-opacity-20 rounded-md p-2">
          <div>
            <h2 class="block text-3xl text-center">Dette er stadigvæk kolonne 1, men på dansk!</h2>
            <p>
              Der er noget nyt tekst i kolonnen! (05-09-2022)
            </p>
          </div>
        </div>
        <div class="flex justify-center bg-pink-300 dark:bg-opacity-20 rounded-md p-2">
          <div>
            <h2 class="block text-3xl text-center">Colum 2</h2>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit.
            Repellendus dolorem optio aspernatur quidem tempora eaque
            reprehenderit, assumenda non maxime dolores necessitatibus debitis
            corrupti eveniet!
          </div>
        </div>
        <div class="flex justify-center bg-pink-400 dark:bg-opacity-20 rounded-md p-2">
          <div>
            <h2 class="block text-3xl text-center">Colum 3</h2>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempora
            perferendis cupiditate placeat fugit corrupti neque veniam iste
            provident cumque facilis necessitatibus praesentium odit impedit
            alias enim debitis, quas suscipit hic. lorem
          </div>
        </div>
      </section>
    </template>
  </MainLayout>
</template>

<style>
body {
  @apply dark:bg-gray-900 dark:text-gray-50;
  @apply bg-pink-100;
}
main {
  @apply py-20;
}
</style>
