<script>
    import { Swiper, SwiperSlide } from 'swiper/svelte';
    import {Autoplay, Navigation} from 'swiper';
    import 'swiper/css';
    import "swiper/css/navigation";
    import programs from './data/programs.json';
    
  </script>
  
  <section class="team-area-two pb-24 px-10">
      <div class="container">
          
          <div class="row justify-content-center">
  <Swiper
      modules="{[Autoplay, Navigation]}"
      spaceBetween={50}
      slidesPerView={1}
      centeredSlides={true}
      loop={true}
      navigation={true}
      autoplay={{
          delay: 6000,
          disableOnInteraction: false,
      }}
      breakpoints={{
          "768": {
            slidesPerView: 4,
            spaceBetween: 20,
          },
          "1300": {
            slidesPerView: 4,
            spaceBetween: 20,
          },
      }}
  >
      {#each programs as program}
          <SwiperSlide>
               <div class="">
                      <div class="team-item-two">
                          <div class="team-thumb-two">
                              <a href="/{program.link}"><img src="img/bg/{program.image}" alt="" class=" w-full h-full"></a>
                              <div class="team-social-two">
                                  <ul class="list-wrap">
                                  
                                      <li><i class="fab fa-telegram-plane"></i></li>
                                  </ul>
                              </div>
                          </div>
                          <div class="team-content-two">
                              <h2 class="title"><a href="/{program.link}">{program.title}
                                  </a></h2>
                              <span>{program.address}</span>
                          </div>
                      </div>
                  </div>
          </SwiperSlide>
      {/each}
  </Swiper>
  </div>
  </div>
  </section>