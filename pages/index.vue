<template>
  <div>
    <div class="page main d-flex">
      <div class="video_top_content">
        <nav class="navbar navbar-expand-lg fixed-top">
          <div class="container">
            <a
              href="/"
              class="navbar-brand pointer"
            >
              <img src="~/assets/logo.svg" height="40" class="d-inline-block align-top">
            </a>
            <div class="collapse navbar-collapse">
              <div class="ml-auto">
                <ul class="navbar-nav">
                  <li class="nav-item">
                    Мастерклассы
                  </li>
                  <li class="nav-item">
                    Контакты
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </nav>
        <div class="my-auto container">
          <b-carousel
            indicators
            :interval="3000"
          >
            <b-carousel-slide>
              <template #default>
                <div class="col-lg-4 text-center text-lg-left d-flex">
                  <h1 class="my-auto fs-64">
                    Территория современного
                    творчества
                  </h1>
                </div>
                <div class="ml-auto text-center my-auto col-lg-5">
                  <img src="~assets/main/1.png" width="90%" />
                </div>
              </template>
            </b-carousel-slide>
            <b-carousel-slide>
              <template #default>
                <div class="col-lg-4 text-center text-lg-left d-flex">
                  <h1 class="my-auto fs-64">
                    Территория современного
                    творчества 2
                  </h1>
                </div>
                <div class="ml-auto text-center my-auto col-lg-5">
                  <img src="~assets/main/1.png" width="90%" />
                </div>
              </template>
            </b-carousel-slide>
          </b-carousel>
        </div>
      </div>
      <div class="video-bg">
<!--        <video-->
<!--          src="~assets/1.mp4"-->
<!--          webkit-playsinline-->
<!--          playsinline-->
<!--          autoplay-->
<!--          muted-->
<!--          loop-->
<!--          height="100%"-->
<!--        >-->

<!--        </video>-->
      </div>
    </div>
    <div class="page about_us d-flex flex-column">
      <div class="container pt-5">
        <h1>О нас</h1>
        <div class="mt-5 fs-22">
          Политическое учение Монтескье, с другой стороны, формирует эмпирический марксизм. Континентально-европейский тип политической культуры, тем более в условиях социально-экономического кризиса, теоретически возможен. Политическое учение Локка означает марксизм, впрочем, это несколько расходится с концепцией Истона. Несмотря на внутренние противоречия, коммунизм ограничивает механизм власти. Политическое учение Локка однозначно отражает бихевиоризм.
        </div>
      </div>
      <div class="about_us_slides">
        <div
          class="container mt-5 d-flex flex-row"
          v-prlx="{
          direction: 'x',
          speed: -2,
          fromBottom: false
        }"
        >
          <img src="~assets/about/about_1.png" class="mr-4" />
          <img src="~assets/about/about_2.png" class="mr-4" />
          <img src="~assets/about/about_3.png" class="mr-4" />
          <img src="~assets/about/about_4.png" class="mr-4" />
        </div>
      </div>
      <div class="m-auto about_us_bg w-100 h-100 d-flex py-4">
        <img src="~assets/about/about_us_bg.svg" width="49" height="86" class="m-auto"/>
      </div>
    </div>
    <div class="hot_items py-5 d-flex">
      <div class="container my-auto">
        <b-carousel
          indicators
          controls
        >
          <b-carousel-slide>
            <template #default>
              <hot-event/>
            </template>
          </b-carousel-slide>
          <b-carousel-slide>
            <template #default>
              <hot-event/>
            </template>
          </b-carousel-slide>
        </b-carousel>
      </div>
    </div>
    <div class="pt-5 page masterclass">
      <div class="container">
        <img src="~assets/star.svg" class="mb-4 ml-4" />
        <vue-masonry-wall :items="items" :options="{width: 400, padding: 12}" :ssr="{columns: 2}">
          <template v-slot:default="{item}">
            <div class="card">
              <div class="card-body">
                <div class="card-text">
                  <img src="~assets/masterclass/1.png" width="100%" />
                  <div class="card-title">{{item.title}} <img class="ml-2" src="~assets/next.svg" /></div>
                  <div>{{item.content}}</div>
                </div>
              </div>
            </div>
          </template>
        </vue-masonry-wall>
      </div>
    </div>
    <div class="map py-4">
      <div class="container mt-4">
        <iframe
          style="border-radius: 44px"
          src="https://yandex.ru/map-widget/v1/?um=constructor%3A25f73e16b8d13d7315948a5c6ce0b98464e86b23d5c944f153d4818740c53e8e&amp;source=constructor"
          width="100%"
          height="500"
          frameborder="0"
        ></iframe>
        <div class="row my-5 text-center text-lg-left">
          <div class="col-lg-2 mb-2">
            <a href="/">
              <img src="~/assets/logo_black.svg" height="40" class="d-inline-block align-top">
            </a>
          </div>
          <div
            class="col-lg-3 mb-2"
          >
            8 980 555 5049 <br>
            info@artlab-vrn.ru
          </div>
          <div
            class="col-lg-3"
          >
            г. Воронеж<br>
            Купянский переулок 11
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueMasonryWall from 'vue-masonry-wall'
import HotEvent from '../components/HotEvent'

export default {
  components: { HotEvent, VueMasonryWall },
  data () {
    return {
      items: [
        { title: 'Item 0', content: '18 августа 15:30' },
        { title: 'Item 1', content: '18 августа 15:30' },
        { title: 'Item 2', content: '18 августа 15:30' },
        { title: 'Item 3', content: '18 августа 15:30' },
        { title: 'Item 4', content: '18 августа 15:30' },
        { title: 'Item 5', content: '18 августа 15:30' },
        { title: 'Item 6', content: '18 августа 15:30' },
        { title: 'Item 7', content: '18 августа 15:30' },
        { title: 'Item 8', content: '18 августа 15:30' },
        { title: 'Item 9', content: '18 августа 15:30' },
        { title: 'Item 10', content: '18 августа 15:30' }
      ],
      settings: {
        dots: true,
        dotsClass: 'slick-dots custom-dot-class',
        edgeFriction: 0.35,
        infinite: false,
        speed: 500,
        slidesToShow: 1,
        slidesToScroll: 1
      }
    }
  }
}
</script>
