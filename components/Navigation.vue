<template>
  <header>
    <nav>
      <div><nuxt-link class="text-4xl" to="/">Brasher</nuxt-link></div>
      <ul class="nav-li">
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="#">About</nuxt-link></li>
        <li><nuxt-link to="#">Blog</nuxt-link></li>
        <li><nuxt-link to="#">Contact</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped lang="postcss">
nav {
  @apply flex justify-around;
}

nav ul {
  @apply flex justify-around;
}

nav li {
  @apply list-none mx-8;
}

.nav-li {
  @apply text-2xl;
}

header {
  @apply text-white bg-gray-900 p-8;
}
</style>

<script>
export default {};
</script>