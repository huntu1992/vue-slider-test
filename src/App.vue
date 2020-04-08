<template>
  <!-- <carousel
    :per-page="1"
    :autoplay="true"
    :loop="true"
    :autoplayTimeout="3000"
    :paginationEnabled="true"
    :easing="'ease-in-out'"
    :spacePadding="0"
  >
    <slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </slide>
    <slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </slide>
    <slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </slide>
    <slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </slide>
    <slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </slide>
    <slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </slide>
  </carousel> -->

  <vue-glide
    v-model="index"
    type="carousel"
    :startAt="0"
    :perView="2"
    :gap="10"
    :rewind="true"
    :peek="10"
    glide:run=""
    :run="(d) => lg(d)"
  >
    <vue-glide-slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </vue-glide-slide>
    <vue-glide-slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </vue-glide-slide>
    <vue-glide-slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </vue-glide-slide>
    <vue-glide-slide>
      <img src="../public/sect1_1.png" alt="이미지" />
    </vue-glide-slide>
    <div class="dots"></div>
  </vue-glide>
</template>

<script>
// import { Carousel, Slide } from 'vue-carousel';
import { Glide, GlideSlide } from 'vue-glide-js';

export default {
  name: 'App',
  components: { [Glide.name]: Glide, [GlideSlide.name]: GlideSlide },
  methods: {
    lg(m) {
      console.log('ㅇㅇ', m);
    },
  },
  data() {
    return { index: 0 };
  },
};
</script>

<style>
.VueCarousel-inner {
  text-align: center;
}
.VueCarousel-slide {
  margin: 0 !important;
  padding: 0 !important;
}

.glide__slide--clone {
  /* min-width: 100% !important; */
  /* width: 100% !important; */
  margin: 0;
}
</style>
