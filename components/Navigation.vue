<template>
  <header>
    <nav>
      <div class="logo"><nuxt-link class="text-4xl" to="/">Brasher</nuxt-link></div>
      <ul class="nav-li">
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="#">Video</nuxt-link></li>
        <li><nuxt-link to="#">Magazine</nuxt-link></li>
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

.logo {
  font-family: 'Metal Mania', cursive;
}
</style>

<script>
export default {};
</script>