<script>
  import About from "$lib/components/about.svelte";
  import Carousel from "$lib/components/Carousel.svelte";
  import Faq from "$lib/components/faq.svelte";
  import Plan from "$lib/components/plan.svelte";
  import Teacher from "$lib/components/teacher.svelte";

  import AOS from "aos";
  import "aos/dist/aos.css";
  import { onMount } from "svelte";

  onMount(() => {
    AOS.init({
      duration: 1000,
      easing: "ease-in-out",
      once: true,
    });
  });
</script>

<div>
  <About />
  <Carousel />
  <Teacher />
  <Plan />
  <Faq />
</div>
