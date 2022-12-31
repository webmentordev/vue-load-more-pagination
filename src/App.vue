<template>
  <nav class="flex items-center py-2 px-4 justify-between bg-gray-100">
    <img src="./assets/logo.png" width="50">
    <div>
      <router-link class="px-6 font-semibold" to="/">Home</router-link>
      <router-link class="px-6 font-semibold" to="/about">About</router-link>
    </div>
  </nav>
  <router-view/>
</template>

