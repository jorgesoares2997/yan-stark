<script lang="ts">
  interface FAQItem {
    question: string;
    answer: string;
  }
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
  let faqs: FAQItem[] = [
    {
      question: "O curso é online?",
      answer:
        "Sim! Você pode assistir às aulas no seu ritmo e acessar de qualquer lugar.",
    },
    {
      question: "Preciso ter experiência com evangelismo para fazer o curso?",
      answer:
        "Não! O curso é feito para qualquer cristão, independente do nível de experiência.",
    },
    {
      question: "Por quanto tempo terei acesso ao curso?",
      answer:
        "O acesso é vitalício! Você poderá assistir e revisar sempre que quiser.",
    },
    {
      question: "Como faço para me inscrever?",
      answer: "Clique no botão abaixo e garanta sua vaga agora!",
    },
  ];

  let activeQuestion: string | null = null;

  function toggleAnswer(question: string) {
    activeQuestion = activeQuestion === question ? null : question;
  }

  const iconsWithText = [
    {
      icon: "cross",
      text: "Como vencer a timidez e falar de Jesus com confiança",
    },
    { icon: "people", text: "O que dizer a diferentes tipos de pessoas" },
    {
      icon: "voice",
      text: "Como evangelizar em qualquer lugar: no trabalho, na escola, na rua ou online",
    },
    {
      icon: "role",
      text: "Métodos práticos para abordar pessoas de maneira natural e respeitosa",
    },
    {
      icon: "edit",
      text: "A importância do evangelismo e seu papel no Reino de Deus",
    },
    {
      icon: "ask",
      text: "Como responder às perguntas mais comuns sobre a fé cristã",
    },
    {
      icon: "tool",
      text: "Como usar o testemunho pessoal como ferramenta poderosa",
    },
    {
      icon: "nearby",
      text: "Estratégias para discipular aqueles que aceitam a Cristo",
    },
  ];
  const items = [
    {
      text: "Quem ama missões, mas tem receio de evangelizar na prática.",
    },
    {
      text: "Novos convertidos que querem aprender desde cedo a compartilhar sua fé.",
    },
    {
      text: "Quem já evangeliza, mas quer se aperfeiçoar e se tornar mais eficaz.",
    },
    {
      text: "Líderes e discipuladores que desejam ensinar outros a evangelizar.",
    },
  ];
  const card = [
    {
      text: "3 encontros no Meet",
    },
    {
      text: "Atualizações do curso",
    },
    { text: "Suporte via Whatsapp" },
  ];
</script>

<div class="">
  <div id="inicio" class="grid bg-black text-white" data-aos="fade-down">
    <div class="flex m-auto w-11/12 items-center justify-center">
      <img src="/Fotos/head.png" alt="Yan stark" />
    </div>
    <div class="grid py-4">
      <div class="flex font-bold m-auto text-center flex-col">
        <h1 class="text-[#FF8C02] text-2xl text-center">
          Evangelize com confiança:
        </h1>
        <h2 class="w-2/3 m-auto">
          Aprenda a compartilhar o Evangelho sem Medo!
        </h2>
      </div>
      <p class="font-extralight text-sm w-2/3 m-auto text-center mt-4">
        Descubra como perder vergonha, compartilhar sua fé com clareza e cumprir
        o chamado de levar Cristo às pessoas, com um método prático.
      </p>
      <a
        href="https://wa.me/5581985777066?text=Fala%20Yan!!%20Quero%20aprender%20a%20evangelizar%20com%20ousadia!"
        target="_blank"
        class="bg-[#FF8C02] cursor-pointer w-11/12 m-auto text-white rounded-md p-3 text-sm font-light my-8 text-center block"
      >
        Quero me inscrever agora
      </a>
      <h1 id="sobre" class="text-xl font-bold text-center mt-4">
        Sobre o curso
      </h1>
      <p class="text-center text-sm font-extralight w-11/12 m-auto my-4">
        Esse curso foi criado para cristãos que desejam evangelizar, mas não
        sabem como começar. Em <strong>aulas práticas e diretas</strong>, você
        aprenderá:
      </p>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 my-4 w-11/12 m-auto">
        {#each iconsWithText as { icon, text }}
          <div
            class="p-6 bg-black border border-[#ff8d0280] h-48 rounded-lg shadow-lg text-center flex flex-col items-center"
          >
            <img
              src={`/icons/${icon}.svg`}
              alt={text}
              class="w-16 h-16 mx-auto text-[#FF8C02]"
            />
            <p class="mt-2 w-11/12 text-center font-bold">{text}</p>
          </div>
        {/each}
      </div>
    </div>
  </div>

  <div class="flex flex-col lg:w-1/3 w-11/12 m-auto mt-8" data-aos="fade-up">
    <img
      src="/Fotos/who.webp"
      class="rounded-[15%] my-4"
      alt="Who is the course"
    />
    <h1 class="font-bold text-left my-4 text-2xl">Pra quem é o curso?</h1>
    <ul class="list-none space-y-4">
      {#each items as item}
        <li class="flex items-center space-x-2">
          <span
            class="flex items-center justify-center min-w-4 min-h-4 text-xs rounded-full bg-[#ff8c02] text-white"
            >✓</span
          >
          <span>{item.text}</span>
        </li>
      {/each}
    </ul>
  </div>

  <div id="teacher" class="flex flex-col bg-[#f7f7f7] mt-4" data-aos="fade-up">
    <img
      class="rounded-[15%] lg:w-1/3 w-11/12 m-auto my-8"
      src="/Fotos/iam.webp"
      alt="Quem sou eu"
    />
    <div class="gap-4 lg:w-1/3 w-11/12 m-auto">
      <h1 class="text-2xl">
        Quem é <span class="text-[#ff8c02] font-bold">Yan Stark?</span>
      </h1>
      <p class="mt-4 font-light">
        Meu nome é Yan, tenho 30 anos, sou noivo de Ítaly Schomberger, rapper,
        poeta e apaixonado por pregar o evangelho. Sou membro da Igreja Batista
        em Prazeres (IBP) e moro em Jaboatão dos Guararapes (PE).
      </p>
      <p class="mt-4 font-light">
        Em 2017, Jesus me resgatou, e em 2018, após o meu batismo, decidi que
        não queria apenas ocupar um banco na igreja — meu coração ardia por
        alcançar vidas. Comecei evangelizando minha própria comunidade e, com o
        tempo, Deus me levou a compartilhar Sua mensagem em diversos lugares do
        país.
      </p>

      <p class="mt-4 font-light">
        Durante essa caminhada, vi muitas pessoas despertarem para o
        evangelismo, mas sem coragem para agir. Por isso, criei este curso: para
        te encorajar a pregar com ousadia e viver na prática a missão que Jesus
        nos confiou. Vamos juntos!
      </p>
    </div>
    <a
      href="https://wa.me/5581985777066?text=Fala%20Yan!!%20Quero%20aprender%20a%20evangelizar%20com%20ousadia!"
      target="_blank"
      class="bg-[#FF8C02] cursor-pointer lg:w-1/3 w-11/12 m-auto text-white rounded-md p-3 text-sm font-light my-8 text-center block"
    >
      Quero me inscrever agora
    </a>
  </div>

  <div id="plano" class="bg-black flex flex-col text-white" data-aos="fade-up">
    <div class="mt-8">
      <h1 class="m-auto text-center text-xl">Invista no seu Chamado!</h1>
      <p class="font-light m-auto w-11/12 text-center">
        Garanta seu acesso a um conteúdo que pode transformar sua vida como
        cristão e te preparar para cumprir o <strong>Ide do Senhor</strong> com ousadia
        e propósito! 🚀
      </p>
    </div>
    <div
      class="flex flex-col lg:w-1/3 w-11/12 mt-8 lg:mb-6 mb-4 m-auto rounded-lg h-[500px]"
    >
      <div
        class="text-black text-lg flex flex-col text-center justify-center font-bold h-[50px] bg-[#ff8c02] rounded-t-2xl"
      >
        <h1 class="text-xl">De R$ <s>97,00</s></h1>
      </div>
      <div class="text-black bg-white rounded-b-2xl">
        <div
          class="m-auto flex flex-col text-center items-center justify-center mt-6"
        >
          <p
            class="font-light text-sm w-24 justify-end flex -mb-4 whitespace-nowrap"
          >
            Apenas 6x de R$
          </p>
          <h1
            class=" text-[50px] font-bold flex items-center justify-center text-center"
          >
            8,64
          </h1>
        </div>
        <p class="text-center text-[#888]">ou R$ 47,00 à vista</p>
        <ul class="list-none flex flex-col mt-8 gap-4">
          {#each card as item}
            <div class="flex flex-col items-center justify-center w-full">
              <li class="flex items-center justify-between lg:w-1/3 gap-x-2">
                <span
                  class="flex items-center justify-center min-w-4 min-h-4 text-xs rounded-full bg-[#ff8c02] text-white"
                  >✓</span
                >
                <span class="font-light text-center whitespace-nowrap"
                  >{item.text}</span
                >
              </li>
              <span class="border-t border-gray-300 w-10/12"></span>
            </div>
          {/each}
          <a
            href="https://wa.me/5581985777066?text=Fala%20Yan!!%20Quero%20aprender%20a%20evangelizar%20com%20ousadia!"
            target="_blank"
            class="bg-[#FF8C02] cursor-pointer w-11/12 m-auto text-white rounded-md p-3 text-sm font-light my-8 text-center block"
          >
            Quero me inscrever agora
          </a>
          <p class="p-4 text-xs text-gray-400">
            * Todos os valores serão convertidos para a manutenção de missões.
          </p>
        </ul>
      </div>
    </div>
  </div>

  <div id="faq" class="flex flex-col -mb-8">
    <h1 class="text-center text-2xl font-bold mt-4">Dúvidas Frequentes</h1>

    <div
      class="space-y-4 lg:w-1/3 w-11/12 m-auto border border-[#00000096] rounded-xl mt-8"
    >
      {#each faqs as { question, answer }, i}
        <div class={`p-3 ${i < faqs.length - 1 ? "border-b" : ""}`}>
          <button
            class="w-full flex items-center justify-between text-left font-semibold text-lg transition-all duration-300 ease-in-out"
            on:click={() => toggleAnswer(question)}
          >
            <span
              class={`text-md flex items-center justify-center  ${activeQuestion === question ? "text-[#ff8c02]" : ""}`}
            >
              {question}
            </span>

            <svg
              class={`min-w-5 min-h-5 transform transition-transform duration-300 ease-in-out ${activeQuestion === question ? "rotate-180" : ""}`}
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              />
            </svg>
          </button>
          <div
            class={`overflow-hidden transition-all duration-800 ease-in-out ${activeQuestion === question ? "max-h-96" : "max-h-0"}`}
          >
            {#if activeQuestion === question}
              <p class="text-gray-700">{answer}</p>
            {/if}
          </div>
        </div>
      {/each}
    </div>
    <a
      target="_blank"
      href="https://wa.me/5581985777066?text=Fala%20Yan!!%20Quero%20aprender%20a%20evangelizar%20com%20ousadia!"
      class="bg-[#FF8C02] cursor-pointer items-center justify-center gap-2 flex text-white lg:w-1/3 w-11/12 m-auto rounded-md p-3 text-sm font-light my-8"
    >
      <svg
        fill="white"
        width="20"
        height="20"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 512 512"
        ><!--!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.--><path
          d="M480 32c0-12.9-7.8-24.6-19.8-29.6s-25.7-2.2-34.9 6.9L381.7 53c-48 48-113.1 75-181 75l-8.7 0-32 0-96 0c-35.3 0-64 28.7-64 64l0 96c0 35.3 28.7 64 64 64l0 128c0 17.7 14.3 32 32 32l64 0c17.7 0 32-14.3 32-32l0-128 8.7 0c67.9 0 133 27 181 75l43.6 43.6c9.2 9.2 22.9 11.9 34.9 6.9s19.8-16.6 19.8-29.6l0-147.6c18.6-8.8 32-32.5 32-60.4s-13.4-51.6-32-60.4L480 32zm-64 76.7L416 240l0 131.3C357.2 317.8 280.5 288 200.7 288l-8.7 0 0-96 8.7 0c79.8 0 156.5-29.8 215.3-83.3z"
        /></svg
      >
      Quero aprender a evangelizar!
    </a>
  </div>
</div>
