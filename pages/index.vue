<template>
  <div>
    <Navigation />
    <section>
      <h1 class="text-5xl text-center m-8">#SKATER OF THE DAY</h1>
      <div class="skateroutput"></div>
    </section>
    <Footer />
  </div>
</template>

<style lang="postcss">
body {
  @apply bg-gray-800 text-white
}
.skateroutput img {
  @apply w-96
} 
</style>

<script>
  const instagramApi = async () => {
  const response = await fetch('/.netlify/functions/skaterapi')
  const data = await response.json()

  const skater = data.find((item) => item.caption.includes('#skateroftheday'))
  // INNER HTML HERE
   document.querySelector('.skateroutput').innerHTML = `
   <figure>
   <img src='${skater.url}'
   <p>${skater.caption}</p>
   </figure>
  `
  console.log(data)
  }
instagramApi()
</script>