<script lang="ts">
  import "swiper/css";
  import "swiper/css/navigation";
  import Swiper from "swiper";
  import { Navigation } from "swiper/modules";
  import { onMount } from "svelte";

  let swiperEl: any;
  let prevEl: HTMLElement | null;
  let nextEl: HTMLElement | null;

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
    prevEl = document.querySelector(".swiper-button-prev");
    nextEl = document.querySelector(".swiper-button-next");

    const swiper = new Swiper(swiperEl, {
      modules: [Navigation],
      slidesPerView: 1.2, // Padrão para telas pequenas
      spaceBetween: 10,
      loop: true,
      navigation: {
        nextEl,
        prevEl,
      },
      breakpoints: {
        640: { slidesPerView: 2, spaceBetween: 15 }, // Tablet
        1024: { slidesPerView: 3, spaceBetween: 20 }, // Desktop médio
        1280: { slidesPerView: 4, spaceBetween: 25 }, // Desktop grande
      },
    });

    // Remover as setas em telas grandes
    const updateNavigation = () => {
      const isLargeScreen = window.innerWidth >= 1024; // lg breakpoint
      if (prevEl && nextEl) {
        prevEl.style.display = isLargeScreen ? "block" : "none";
        nextEl.style.display = isLargeScreen ? "block" : "none";
      }
    };

    updateNavigation(); // Aplicar no carregamento
    window.addEventListener("resize", updateNavigation);

    return () => window.removeEventListener("resize", updateNavigation);
  });
</script>

<div class="bg-black p-4 text-center m-auto">
  <div class="mt-6">
    <div bind:this={swiperEl} class="swiper">
      <div class="swiper-wrapper">
        {#each slides as slide}
          <div
            class="swiper-slide flex items-center justify-center rounded-xl shadow-lg bg-[#FF8C02] overflow-hidden"
          >
            <img
              src={slide.image}
              alt="Slide {slide.id}"
              class="w-full object-cover"
            />
          </div>
        {/each}
      </div>

      <!-- Botões de navegação (somem no lg) -->
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
