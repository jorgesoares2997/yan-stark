<script lang="ts">
  import "swiper/css";
  import "swiper/css/navigation";
  import Swiper from "swiper";
  import { Navigation } from "swiper/modules";
  import { onMount } from "svelte";

  let swiperEl: any;

  const slides = [
    { id: 1, image: "/carroussel/1.PNG" },
    { id: 2, image: "/carroussel/2.PNG" },
    { id: 3, image: "/carroussel/3.PNG" },
    { id: 4, image: "/carroussel/4.PNG" },
    { id: 5, image: "/carroussel/5.PNG" },
    { id: 6, image: "/carroussel/6.PNG" },
    { id: 7, image: "/carroussel/7.PNG" },
    { id: 8, image: "/carroussel/8.PNG" },
    { id: 9, image: "/carroussel/9.PNG" },
    { id: 10, image: "/carroussel/10.PNG" },
    { id: 11, image: "/carroussel/11.PNG" },
  ];

  onMount(() => {
    new Swiper(swiperEl, {
      modules: [Navigation],
      slidesPerView: 3,
      spaceBetween: 20,
      loop: true,
      navigation: true,
    });
  });
</script>

<div class="text-center w-11/12 m-auto">
  <div class="mt-6">
    <div bind:this={swiperEl} class="swiper">
      <div class="swiper-wrapper">
        {#each slides as slide}
          <div
            class="swiper-slide flex items-center justify-center rounded-xl shadow-lg bg-red-600 overflow-hidden"
          >
            <img
              src={slide.image}
              alt="Slide {slide.id}"
              class="w-full object-cover"
            />
          </div>
        {/each}
      </div>

      <!-- Botões de navegação -->
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
  </div>

  <a
    href="https://wa.me/5581985777066?text=Fala%20Yan!!%20Quero%20aprender%20a%20evangelizar%20com%20ousadia!"
    target="_blank"
    class="bg-[#FF8C02] cursor-pointer m-auto w-11/12 lg:w-1/3 whitespace-nowrap text-white rounded-md p-3 text-sm font-light my-8 text-center block"
  >
    QUERO GARANTIR MEU ACESSO
  </a>
</div>
