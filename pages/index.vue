<template>
  <div class="w-100">
    <div class="hero py-64 flex items-center justify-center">
      <div class="container px-2">
        <h2 
          class="mb-4 text-center text-4xl tracking-tight leading-tight font-extrabold text-gray-900
            sm:text-6xl lg:text-5xl xl:text-6xl"
        >
          Front End / Full Stack Developer
        </h2>
        <p class="text-center text-2xl tracking-tight leading-tight font-medium text-gray-700">
          I help solve problems for small businesses
        </p>

        <img class="circle-portrait mx-auto mt-20" :src="portrait" />

        <div class="container mt-16 mx-auto">
          <h2 
            class="mb-4 text-center text-2xl tracking-tight leading-tight font-extrabold text-black
              sm:text-2xl lg:text-3xl xl:text-3xl"
          >
            Hello! I'm Dennis.  Lovely to meet you.
          </h2>
          <p class="bio text-center text-2xl tracking-tight leading-tight font-thin text-black">
            I am an engineer with full stack experience specializing in front end development. <br/>
            My main experiences and speciality is working closely with small businesses in building an online presence and creating web applications to solve various business problems and making my client's life easier.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SquareP from '@/assets/images/square-p.png'
export default {
  data() {
    return {
      portrait: SquareP
    }
  }

}
</script>

<style>
.hero {
  height: 1000px;
}

.circle-portrait {
  width: 200px; 
  height: 200px;
  border-radius: 1000px;
}

.summary {
  background-color: #7510F7;
  height: 500px;
}

.bio {
  max-width: 850px;
  margin: 0 auto;
}
</style>
