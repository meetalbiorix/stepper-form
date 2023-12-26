<template>
  <main >
    <h1 class="text-3xl font-bold underline">{{ website.name }}</h1>
    <p>{{ website.description }}</p>
    <button @click="website.changeName">Change name</button>
  </main>
</template>

<script setup>
const website = useWebsiteStore()

await callOnce(website.fetch)
</script>