<template>
  <div class="portfolio pb-20">
    <h2 class="mt-24 text-5xl font-extrabold text-center">Works</h2>

    <div class="container px-4 mx-auto mt-24 divide-y-2 sm:px-8">

      <div class="listicle border-t-2 pt-10">
        <div class="heading flex items-center justify-between">
          <div>
            <h2 class="text-3xl font-bold">Listicle Clothing</h2>
            <p class="text-xl font-base">E-commerce website for Women's Apparel</p>
          </div>
          <span class="inline-flex shadow-sm view-button">
            <button @click="sendTo('https://www.listicleclothing.com')" type="button" class="inline-flex items-center px-4 py-2 border border-transparent text-base leading-6 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:border-indigo-700 focus:shadow-outline-indigo active:bg-indigo-700 transition ease-in-out duration-150">
              <!-- Heroicon name: mail -->
              Visit Website

            </button>
          </span>
        </div>

        
        <img class="main-image mt-8 shadow-md" :src="listicleMain" />
        
        <div class="about-image flex pt-16">
          <div class="left-block">
            <h2 class="text-3xl font-bold">About the Project</h2>
            <p class="text-xl font-base">
              Listicleclothing.com is a full feature e-commerce site with an indepth admin capabilities that rivals that of shopify.  
              It is the first project I was the lead developer in.  It includes many features like setting up product variants, customer notification, managing products/orders/customers, and marketing emailer using SendGrid.
            </p>
            <p class="text-xl font-base mt-4">
              The main challenge in this project was building out a very customized user experience in the admin for the client's use with their business. Important focus on ease of use and making their work easier.
            </p>
          </div>
          <div class="right-block flex items-center justify-end">
            <div class="image-spacer">
                <p class='text-center mb-4'>Click to flip through the images</p>
                <transition-group 
                  name="fade" 
                  mode="in-out"
                  class="transition-block"
                >
                  <img 
                    v-for="(image, index) in listicleImages"
                    v-show="index == currentListicle" 
                    :key="`listicle-${index}`"
                    @click="switchImage(index, listicleImages)"
                    class="image-show cursor-pointer" 
                    :src="image" 
                  />
                </transition-group>
                
              
            </div>
          </div>
        </div>
        <div class="technology mb-16">
          <h2 class="text-2xl font-semibold mb-4">Tech List:</h2>
          <template v-for="(tech, index) in technology.listicle">
            <span :key="`listicle-tech-${index}`" class="pill" :style="`background-color: ${pillBGColor(tech)}`">{{tech}}</span>
          </template>
        </div>
      </div>

      <div class="mylookingglass pt-20">
        <div class="heading flex items-center justify-between">
          <div>
            <h2 class="text-3xl font-bold">My Looking Glass</h2>
            <p class="text-xl font-base">User Feedback Marketing Platform</p>
          </div>
          <span class="inline-flex shadow-sm view-button">
            <button @click="sendTo('https://www.mlgfiles.com')" type="button" class="inline-flex items-center px-4 py-2 border border-transparent text-base leading-6 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:border-indigo-700 focus:shadow-outline-indigo active:bg-indigo-700 transition ease-in-out duration-150">
              <!-- Heroicon name: mail -->
              Visit Website

            </button>
          </span>
        </div>

        
        <img class="main-image mt-8 shadow-md" :src="MlgMain" />
        
        <div class="about-image flex py-16">
          <div class="left-block">
            <h2 class="text-3xl font-bold">About the Project</h2>
            <p class="text-xl font-base">
              My Looking Glass is a marketing platform for obtaining valuable user feedback from professional make up artists for various cosmetic companies.
              My primary responsibility was to build out the front-end components for this web application and jump on the backend writing api routes as necessary.  Worked closely with the designer in providing a good 
              user interface for both make up professionals and the My Looking Glass employee.
            </p>
            <p class="text-xl font-base mt-4">
              This was a fairly challenging project due to a very unique design that required some "out of the box" thinking/solution using HTML/CSS.
            </p>
          </div>
          <div class="right-block flex items-center justify-end">
            <div class="image-spacer">
                <p class='text-center mb-4'>Click to flip through the images</p>
                <transition-group 
                  name="fade" 
                  mode="in-out"
                  class="transition-block"
                >
                  <img 
                    v-for="(image, index) in MlgImages"
                    v-show="index == currentMLG" 
                    :key="`listicle-${index}`"
                    @click="switchMLGImage(index, MlgImages)"
                    class="image-show cursor-pointer" 
                    :src="image" 
                  />
                </transition-group>
                
              
            </div>
          </div>
        </div>

        <div class="technology mb-16">
          <h2 class="text-2xl font-semibold mb-4">Tech List:</h2>
          <template v-for="(tech, index) in technology.mlg">
            <span :key="`listicle-tech-${index}`" class="pill" :style="`background-color: ${pillBGColor(tech)}`">{{tech}}</span>
          </template>
        </div>
        
      </div>

      <div class="funkhaus pt-20">
        <div class="heading flex items-center justify-between">
          <div>
            <h2 class="text-3xl font-bold">Funkhaus - Component Factory</h2>
            <p class="text-xl font-base">Front end freelance work creating components for various web projects</p>
          </div>
        </div>

        
        <img class="main-image mt-8 shadow-md" :src="FunkMain" />
        
        <div class="about-image flex py-16">
          <div class="left-block">
            <h2 class="text-3xl font-bold">About the Project</h2>
            <p class="text-xl font-base">
              Funkhaus is a digital creative agency. In 2019, they started a new concept of a "Component Factory" which streamlines the freelance process, paying freelances for creating individual components.  
              A style guide is provided along with the requirements for the components. I have worked with Funkhaus as a freelancer on and off, building out components for them.  
            </p>
            <p class="text-xl font-base mt-4">
              
            </p>
          </div>
          <div class="right-block flex items-center justify-end">
            <div class="image-spacer">
                <p class='text-center mb-4'>Click to flip through the images</p>
                <transition-group 
                  name="fade" 
                  mode="in-out"
                  class="transition-block"
                >
                  <img 
                    v-for="(image, index) in FunkImages"
                    v-show="index == currentFunk" 
                    :key="`listicle-${index}`"
                    @click="switchFunkImage(index, FunkImages)"
                    class="image-show cursor-pointer" 
                    :src="image" 
                  />
                </transition-group>
                
              
            </div>
          </div>
        </div>

        <div class="technology mb-16">
          <h2 class="text-2xl font-semibold mb-4">Tech List:</h2>
          <template v-for="(tech, index) in technology.funkhaus">
            <span :key="`listicle-tech-${index}`" class="pill" :style="`background-color: ${pillBGColor(tech)}`">{{tech}}</span>
          </template>
        </div>
        
      </div>

      <div class="fanbird pt-20">
        <div class="heading flex items-center justify-between">
          <div>
            <h2 class="text-3xl font-bold">FANBIRD</h2>
            <p class="text-xl font-base">A new marketing platform</p>
          </div>
          <span class="inline-flex shadow-sm view-button">
            <button @click="sendTo('https://fanbird.co')" type="button" class="inline-flex items-center px-4 py-2 border border-transparent text-base leading-6 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:border-indigo-700 focus:shadow-outline-indigo active:bg-indigo-700 transition ease-in-out duration-150">
              <!-- Heroicon name: mail -->
              Visit Website

            </button>
          </span>
        </div>

        
        <img class="main-image mt-8 shadow-md" :src="FanbirdMain" />
        
        <div class="about-image flex py-16">
          <div class="left-block">
            <h2 class="text-3xl font-bold">About the Project</h2>
            <p class="text-xl font-base">
              Fanbird is a marketing platform where businesses can promote their brand and receive valuable customer information.  Users can win points by completing missions and these points can be used to exchange for prizes and products.  
            </p>
            <p class="text-xl font-base mt-4">
              Fanbird is still in progress.
            </p>
          </div>
          <div class="right-block flex items-center justify-end">
            <div class="image-spacer">
                <p class='text-center mb-4'>Click to flip through the images</p>
                <transition-group 
                  name="fade" 
                  mode="in-out"
                  class="transition-block"
                >
                  <img 
                    v-for="(image, index) in FanbirdImages"
                    v-show="index == currentFanbird" 
                    :key="`listicle-${index}`"
                    @click="switchFanBirdImage(index, FanbirdImages)"
                    class="image-show cursor-pointer" 
                    :src="image" 
                  />
                </transition-group>
                
              
            </div>
          </div>
        </div>

        <div class="technology mb-16">
          <h2 class="text-2xl font-semibold mb-4">Tech List:</h2>
          <template v-for="(tech, index) in technology.teetime">
            <span :key="`listicle-tech-${index}`" class="pill" :style="`background-color: ${pillBGColor(tech)}`">{{tech}}</span>
          </template>
        </div>
        
      </div>

      <div class="teetime pt-20">
        <div class="heading flex items-center justify-between">
          <div>
            <h2 class="text-3xl font-bold">The Reserver - Tee Time</h2>
            <p class="text-xl font-base">Reservation Platform for Disc Golf Course</p>
          </div>
          <span class="inline-flex shadow-sm view-button">
            <button @click="sendTo('https://tee-time.netlify.app')" type="button" class="inline-flex items-center px-4 py-2 border border-transparent text-base leading-6 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:border-indigo-700 focus:shadow-outline-indigo active:bg-indigo-700 transition ease-in-out duration-150">
              <!-- Heroicon name: mail -->
              Visit Website

            </button>
          </span>
        </div>

        
        <img class="main-image mt-8 shadow-md" :src="TeetimeMain" />
        
        <div class="about-image flex py-16">
          <div class="left-block">
            <h2 class="text-3xl font-bold">About the Project</h2>
            <p class="text-xl font-base">
              Tee Time is a reservation platform where users can sign up and reserve a "tee time" in The Reserve disc golf course.  In addition to being able to reserve a "tee time", the 
              web app also provides information about the course and individual holes.  This project is still in development.
            </p>
            <p class="text-xl font-base mt-4">
              The web app is primarily to be used on the mobile device.  The content of the site can be changed by the client by using the admin.  
            </p>
            <p class="text-xl font-base mt-4">
              Login: admin@admin.com <br/>
              Password: asdfasdf
            </p>
          </div>
          <div class="right-block flex items-center justify-end">
            <div class="image-spacer">
                <p class='text-center mb-4'>Click to flip through the images</p>
                <transition-group 
                  name="fade" 
                  mode="in-out"
                  class="transition-block"
                >
                  <img 
                    v-for="(image, index) in TeetimeImages"
                    v-show="index == currentTeetime" 
                    :key="`listicle-${index}`"
                    @click="switchTeetimeImage(index, TeetimeImages)"
                    class="image-show cursor-pointer" 
                    :src="image" 
                  />
                </transition-group>
                
              
            </div>
          </div>
        </div>

        <div class="technology mb-16">
          <h2 class="text-2xl font-semibold mb-4">Tech List:</h2>
          <template v-for="(tech, index) in technology.teetime">
            <span :key="`listicle-tech-${index}`" class="pill" :style="`background-color: ${pillBGColor(tech)}`">{{tech}}</span>
          </template>
        </div>
        
      </div>


      

    </div>
  </div>
</template>

<script>
import Listicle1 from '@/assets/images/listicle-1.png'
import Listicle2 from '@/assets/images/listicle-2.png'
import Listicle3 from '@/assets/images/listicle-3.png'
import Listicle4 from '@/assets/images/listicle-4.png'
import Listicle5 from '@/assets/images/listicle-5.png'

import MLG1 from '@/assets/images/mlg-1.png'
import MLG2 from '@/assets/images/mlg-2.png'
import MLG3 from '@/assets/images/mlg-3.png'
import MLG4 from '@/assets/images/mlg-4.png'
import MLG5 from '@/assets/images/mlg-5.png'
import MLG6 from '@/assets/images/mlg-6.png'
import MLG7 from '@/assets/images/mlg-7.png'
import MLG8 from '@/assets/images/mlg-8.png'
import MLG9 from '@/assets/images/mlg-9.png'

import Funk1 from '@/assets/images/funkhaus-1.png'
import Funk2 from '@/assets/images/funkhaus-2.png'
import Funk3 from '@/assets/images/funkhaus-3.png'
import Funk4 from '@/assets/images/funkhaus-4.png'
import Funk5 from '@/assets/images/funkhaus-5.png'
import Funk6 from '@/assets/images/funkhaus-6.png'

import Teetime1 from '@/assets/images/teetime-1.png'
import Teetime2 from '@/assets/images/teetime-2.png'
import Teetime3 from '@/assets/images/teetime-3.png'
import Teetime4 from '@/assets/images/teetime-4.png'

import Fanbird1 from '@/assets/images/fanbird-1.png'
import Fanbird2 from '@/assets/images/fanbird-2.png'
import Fanbird3 from '@/assets/images/fanbird-3.png'

export default {
  data () {
    return {
      listicleMain: Listicle1,
      listicleImages: [
        Listicle2, Listicle3, Listicle4, Listicle5
      ],
      MlgMain: MLG1,
      MlgImages: [
        MLG2, MLG3, MLG4, MLG5, MLG6, MLG7, MLG8, MLG9
      ],
      FunkMain: Funk1,
      FunkImages: [
        Funk2, Funk3, Funk4, Funk5, Funk6
      ],
      TeetimeMain: Teetime1,
      TeetimeImages: [
        Teetime2, Teetime3, Teetime4
      ],
      FanbirdMain: Fanbird1,
      FanbirdImages: [
        Fanbird1, Fanbird2, Fanbird3
      ],
      currentListicle: 0,
      currentMLG: 0,
      currentFunk: 0,
      currentTeetime: 0,
      currentFanbird: 0,
      technology: {
        listicle: [
          'Javascript', 'NuxtJS', 'TailwindCSS', 'Express', 'Postgres', 'Sequelize', 'SendGrid'
        ],
        mlg: [
          'HTML', 'CSS', 'Javascript', 'NuxtJS', 'NestJS', 'TypeORM'
        ],
        funkhaus: [
          'HTML', 'SCSS', 'Javascript', 'NuxtJS', 'Storybook'
        ],
        teetime: [
          'NuxtJS', 'TailwindCSS', 'Express', 'Postgres', 'Sequelize'
        ],
        fanbird: [
          'NuxtJS', 'TailwindCSS', 'NestJS', 'Postgres', 'TypeORM'
        ]
      }
    }
  },
  methods: {
    switchImage(index, array) {
      if (index == array.length - 1) {
        this.currentListicle = 0
      } else {
        this.currentListicle = index + 1
      }
    },
    switchMLGImage(index, array) {
      if (index == array.length - 1) {
        this.currentMLG = 0
      } else {
        this.currentMLG = index + 1
      }
    },
    switchFunkImage(index, array) {
      if (index == array.length - 1) {
        this.currentFunk = 0
      } else {
        this.currentFunk = index + 1
      }
    },
    switchTeetimeImage(index, array) {
      if (index == array.length - 1) {
        this.currentTeetime = 0
      } else {
        this.currentTeetime = index + 1
      }
    },
    switchFanBirdImage(index, array) {
      if (index == array.length - 1) {
        this.currentFanbird = 0
      } else {
        this.currentFanbird = index + 1
      }
    },
    sendTo(link) {
      window.open(link, '_blank')
    },
    pillBGColor(tech) {
      switch (tech) {
        case 'HTML': return '#E96228'
        case 'CSS': return '#2862E9'
        case 'SCSS': return '#2862E9'
        case 'NestJS': return '#E0234E'
        case 'TypeORM': return '#FFAB00'
        case 'Javascript': return '#EFD81D'
        case 'NuxtJS': return '#4CAF50'
        case 'TailwindCSS': return '#16BDCA'
        case 'Express': return '#F27878'
        case 'Postgres': return '#31648C'
        case 'Sequelize': return '#03AFEF'
        case 'SendGrid': return '#9B4AF8'
        case 'Storybook': return '#FF4785'
      } 
    }
  }
}
</script>

<style scoped>
.main-image {
  border-radius: 10px;
  width: 100%;
}

.right-block, .left-block {
  flex: 0 0 50%;
  padding: 1rem;
}

.image-spacer {
  min-height: 450px;
  width: 100%;
  position: relative;
}

.transition-block {
  width: 100%;
  position: absolute;
}

.image-show {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  max-height: 400px;
}

.pill {
  padding: 8px 16px;
  margin: 4px 8px;
  border-radius: 100px;
  color: white;
  display: inline-block;
}

@media screen and (max-width: 768px) {
  .about-image {
    flex-direction: column;
  }
}

@media screen and (max-width: 500px) {
  .heading {
    flex-direction: column;
    text-align: center;
  }
  .heading span, .heading button {
    width: 100%;
  }
  .heading button {
    margin-top: 8px;
    justify-content: center;
  }
  .image-spacer {
    min-height: 375px;
  }
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.4s ease-in-out;
}
</style>