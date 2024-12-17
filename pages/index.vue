<script setup lang="ts">
import { ref } from 'vue'
import Swiper from '~/components/swiper/swiper.vue'
import { Pagination, Mousewheel } from 'swiper/modules'
import ShowCelebrities from '~/components/showCelebrities.vue'
import ExploreByCategory from '~/components/explore-by-category.vue'

const values = ref([
  {
    image:
      'https://images.pexels.com/photos/1525041/pexels-photo-1525041.jpeg?cs=srgb&dl=pexels-francesco-ungaro-1525041.jpg&fm=jpg',
  },
  {
    image:
      'https://asset.gecdesigns.com/img/wallpapers/beautiful-fantasy-wallpaper-ultra-hd-wallpaper-4k-sr10012418-1706506236698-cover.webp',
  },
  {
    image: 'https://images3.alphacoders.com/135/1350069.jpeg',
  },
  {
    image:
      'https://static.vecteezy.com/system/resources/thumbnails/025/061/745/small_2x/4k-beautiful-colorful-abstract-wallpaper-photo.jpg',
  },
  {
    image:
      'https://static.vecteezy.com/system/resources/thumbnails/025/061/745/small_2x/4k-beautiful-colorful-abstract-wallpaper-photo.jpg',
  },
]);

const goToNextSlide = () => {
  const swiper = document.querySelector('#mySwiper')?.swiper
  swiper.slideNext()
}

const goToPrevSlide = () => {
  const swiper = document.querySelector('#mySwiper')?.swiper
  swiper.slidePrev()
}
</script>
<template>
  <div class="home-page">
    <div class="container-1 mt-24">
      <div class="wrapper">
        <div class="part1 flex gap-4 flex-col">
          <h1 class="custom-darkBlue-text text-5xl font-semibold">
            Beyoncé Live in Concert!
          </h1>
          <h3 class="custom-darkPurple-text text-2xl font-bold">
            A Night to Remember!
          </h3>
          <h6 class="max-w-md custom-lightPurple-text">
            Get ready for an extraordinary night with Beyoncé with breathtaking
            performances and unforgettable moments.
            <span class="block mt-2">Don’t wait – secure your tickets</span>
          </h6>
          <button
            class="custom-lightPink-bg w-44 text-white px-12 py-4 rounded-xl font-semibold my-5 text-base"
          >
            Get Ticket
          </button>
        </div>
      </div>
      <div class="part2 custom-middarkGray-bg mt-5">
        <div class="wrapper">
          <div class="relative flex justify-between items-start gap-20">
            <div class="part1 flex items-start flex-col w-1/2 pt-10">
              <h3 class="custom-lightGray-text text-lg">
                Find your favorite concert
              </h3>
              <div
                class="searchBtn custom-lightGray-bg flex flex-row gap-3 p-4 w-full rounded-xl mt-4 mb-3"
              >
                <NuxtImg
                  src="/search-normal.png"
                  sizes="20px"
                  class="object-contain"
                />
                <input
                  type="text"
                  class="border-none outline-none bg-transparent custom-placeholder-text w-full"
                  placeholder="Search by Artist, Event or Venue"
                />
              </div>
              <div class="hashtags flex items-center gap-2">
                <div
                  class="custom-lightGray-text custom-lightGray-bg px-2 py-1 rounded-xl"
                >
                  #Summer
                </div>
                <div
                  class="custom-lightGray-text custom-lightGray-bg px-2 py-1 rounded-xl"
                >
                  #Jazz
                </div>
                <div
                  class="custom-lightGray-text custom-lightGray-bg px-2 py-1 rounded-xl"
                >
                  #TaylorSwift
                </div>
                <div
                  class="custom-lightGray-text custom-lightGray-bg px-2 py-1 rounded-xl"
                >
                  #NewYork
                </div>
              </div>
            </div>
            <div class="part2 w-1/2 minus-margin">
              <Swiper
                :values="values"
                class="overflow-hidden swiper rounded-t-3xl"
                id="mySwiper"
                :modules="[Pagination, Mousewheel]"
                direction="vertical"
                swiperSlideClass="h-full w-full"
              />
              <div class="arrows">
                <div class="arrow-top" @click="goToPrevSlide">
                  <NuxtImg src="/arrow-down.png" class="rotate-180" />
                </div>
                <div class="arrow-bottom">
                  <NuxtImg
                    src="/arrow-down.png"
                    sizes="17px"
                    @click="goToNextSlide"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container-2 mt-24">
      <div class="wrapper">
        <div class="part1">
          <showCelebrities :values="values" subject="Upcoming concerts" />
        </div>
        <div class="part2">
          <showCelebrities :values="values" subject="Popular near you" />
        </div>
        <div class="part3">
          <ExploreByCategory :values="values" subject="Explore by category" />
        </div>
      </div>
    </div>
  </div>
</template>
