<template>
  <div>
    <Navigation />
    <section>
      <h1>#SKATER OF THE DAY</h1>
      <div class="skateroutput"></div>
    </section>
    <Footer />
  </div>
</template>

<style lang="postcss">
body {
  @apply bg-gray-800 text-white
}
</style>

<script>
  const instagramApi = async () => {
  const response = await fetch('/.netlify/functions/skaterapi')
  const data = await response.json()

  const skater = data.data.find((item) => item.caption.includes('#skateroftheday'))
  // INNER HTML HERE
  document.querySelector('.skateroutput').innerHTML = `
  <figure>
  <img src='${skater.media_url}'
  <p>${skater.caption}</p>
  </figure>
  `
  console.log(data)
  }
instagramApi()
</script>