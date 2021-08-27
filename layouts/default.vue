<template>
  <div>
    <Nav v-if="$route.name !== 'my-items'" />
    <Nuxt />
  </div>
</template>

<style></style>
