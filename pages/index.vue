<template>
  <div>
    <Navigation />
    <section class="hero-pic">
      <div class="hero-text">
        <span class="hero-section rounded-lg">
          <h1 class="text-5xl m-6">BRASHER MAGAZINE</h1>
          <p class="text-2xl text-center">Skate or Die !</p>
        </span>
      </div>
    </section>
    <section class="day-section">
      <h2 class="text-5xl text-center m-6">SKATER OF THE DAY</h2>
      <div class="skateroutput">
      </div>
    </section>
    <Footer />
  </div>
</template>

<style lang="postcss">
body {
  @apply bg-gray-800 text-white m-0
}

.day-section {
  @apply mt-16 mb-20
}

.skateroutput figure{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column;
}

.skateroutput img {
  @apply w-96
} 

.hero-pic h1, h2, p {
  font-family: 'Metal Mania', cursive;
  text-align: center;
}

.hero-section {
  background-color: hsla(1, 10%, 10%, 0.8);
  margin-top: 15rem;
}

.hero-text {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column;
}

.hero-text h1 {
  padding: 15px 20px 0px 20px;
}

.hero-text p {
  @apply mb-6
}

.hero-pic {
  background-image: url(../static/assets/images/hero-skater.jpg);
  background-position: center;
  background-repeat: no-repeat;
  height: 70vh;
  width: 100%;
}

.skateroutput p {
  font-family: 'Bitter', serif;
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
   <p class="m-6 text-xl">${skater.caption.replace('#skateroftheday', '')}</p>
   </figure>
  `
  console.log(data)
  }
instagramApi()
</script>