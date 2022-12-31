<template>
  <div class="about py-6 px-4 max-w-lg m-auto">
    <h1 class="text-gray-800 font-bold mb-3 text-3xl">About Project</h1>
    <p class="text-gray-600 mb-3 text-sm leading-7">Simple VueJS project to create pagination. You <b>Click</b> LoadMore button, then fetch() function will request more posts and append already fetched posts. In this project, when component is mounted, fetch() function will fetch only 3 posts of first page and show in grid. LoadMore function is protected, clicking it will increment page number if no more posts are available than LoadMore button will disappear and No more data message will showup. Components templates are build will Tailwindcss.</p>
    <p class="text-gray-600 text-sm leading-7">For Backend we will <b>JSON Server!</b>. Server will run on port 3000.</p>
    <ul class="text-sm y-3">
      <li class="mb-2"><b>Run Vue: </b> npm run serve</li>
      <li class="mb-2"><b>Run Tailwind:</b> npm run watch</li>
      <li class="mb-2"><b>Run JSONServer:</b> npm run back</li>
    </ul>
  </div>
</template>
