<template>
  <div class="mx-auto space-y-8">
    <div class="space-y-4 mt-4 mx-4 md:mt-6 md:mx-6">
      <h1 class="text-lg md:text-4xl text-center font-bold capitalize">Installation</h1>
      <p class="text-sm md:text-lg text-center text-muted-foreground">
        Get started with Laravel CRUD Bot in a few simple steps
      </p>
    </div>

    <div class="space-y-4 mt-4 mx-4 md:mt-6 md:mx-6">
      <h2 class="text-2xl font-semibold">1. Install via Composer</h2>
      <p>Add the package to your Laravel project using Composer:</p>
      <CodeBlock :commands="installCommand" />
    </div>

    <div class="space-y-4 mt-4 mx-4 md:mt-6 md:mx-6">
      <h2 class="text-2xl font-semibold">2. Publish Configuration</h2>
      <p>Publish the configuration file:</p>
      <CodeBlock :commands="publishCommand" />
    </div>
    <div class=" space-y-4 mt-4 mx-4 grid gap-8 sm:grid-cols-2">
        <NuxtLink
          to="/"
          class="block px-6 py-8 border not-prose rounded-lg border-gray-200 hover:bg-gray-100/50"
        >
          <div
            class="inline-flex items-center rounded-full p-1.5 bg-gray-100 dark:bg-gray-800 group-hover:bg-primary/10 ring-1 ring-gray-300 dark:ring-gray-700 mb-4 group-hover:ring-primary/50"
          >
            <span
              class="fa-solid fa-arrow-left w-5 h-5 text-gray-900"
              aria-hidden="true"
            ></span>
          </div>
          <p class="font-medium text-gray-900 dark:text-white text-[15px] mb-1">
            Introduction
          </p>
          <p
            class="text-sm font-normal text-gray-500 dark:text-gray-400 line-clamp-2"
          >
            Codebider goal is to automate the process of generation of crud.
          </p>
        </NuxtLink>
        <NuxtLink
          to="/usage"
          class="block px-6 py-8 border not-prose rounded-lg border-gray-200 hover:bg-gray-100/50 text-right"
        >
          <div
            class="inline-flex items-center rounded-full p-1.5 bg-gray-100 dark:bg-gray-800 group-hover:bg-primary/10 ring-1 ring-gray-300 dark:ring-gray-700 mb-4 group-hover:ring-primary/50"
          >
            <span
              class="fa-solid fa-arrow-right w-5 h-5 text-gray-900 dark:text-white group-hover:text-primary"
              aria-hidden="true"
            ></span>
          </div>
          <p class="font-medium text-gray-900 dark:text-white text-[15px] mb-1">
            Usage
          </p>
          <p
            class="text-sm font-normal text-gray-500 dark:text-gray-400 line-clamp-2"
          >
            Code Smarter Not Harder!
          </p>
        </NuxtLink>
      </div>
  </div>
</template>
  <script setup>
useHead({
  title: "Installation",
});
const installCommand = ["composer require codebider/generate-crud"];
const publishCommand = [
  "php artisan vendor:publish --tag=crud-generator-config",
];

const previewDatabase = [
  "DB_CONNECTION=mysql",
  "DB_HOST=127.0.0.1",
  "DB_PORT=3306",
  "DB_DATABASE=your_database",
  "DB_USERNAME=your_username",
  "DB_PASSWORD=your_password",
];
</script>

  