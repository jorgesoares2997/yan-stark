<script>
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
</script>

<div class=""></div>
<div id="inicio" class="grid bg-black text-white" data-aos="fade-down">
  <div class="flex m-auto w-11/12 items-center justify-center">
    <img src="/Fotos/head.png" alt="Yan stark" />
  </div>
  <div class="grid py-4">
    <div class="flex font-bold m-auto text-center flex-col">
      <h1 class="text-[#FF8C02] text-2xl text-center">
        Evangelize com confiança:
      </h1>
      <h2 class="w-2/3 m-auto">Aprenda a compartilhar o Evangelho sem Medo!</h2>
    </div>
    <p class="font-extralight text-sm w-2/3 m-auto text-center mt-4">
      Descubra como perder vergonha, compartilhar sua fé com clareza e cumprir o
      chamado de levar Cristo às pessoas, com um método prático.
    </p>
    <a
      href="https://wa.me/5581985777066?text=Fala%20Yan!!%20Quero%20aprender%20a%20evangelizar%20com%20ousadia!"
      target="_blank"
      class="bg-[#FF8C02] cursor-pointer w-11/12 m-auto text-white rounded-md p-3 text-sm font-light my-8 text-center block"
    >
      Quero me inscrever agora
    </a>
    <h1 id="sobre" class="text-xl font-bold text-center mt-4">Sobre o curso</h1>
    <p class="text-center text-sm font-extralight w-11/12 m-auto my-4">
      Esse curso foi criado para cristãos que desejam evangelizar, mas não sabem
      como começar. Em <strong>aulas práticas e diretas</strong>, você
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

<div class="lg:flex w-11/12 m-auto justify-between mt-8" data-aos="fade-up">
  <div class="w-11/12 m-auto lg:w-1/2">
    <img
      src="/Fotos/who.webp"
      class="rounded-[15%] my-4"
      alt="Who is the course"
    />
  </div>
  <div class="flex flex-col lg:w-1/2 w-11/12 h-full pl-8 m-auto">
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
      <a
        href="https://wa.me/5581985777066?text=Fala%20Yan!!%20Quero%20aprender%20a%20evangelizar%20com%20ousadia!"
        target="_blank"
        class="bg-[#FF8C02] cursor-pointer lg:w-1/3 text-white rounded-md p-3 text-sm font-light my-8 text-center block"
      >
        Quero me inscrever agora
      </a>
    </ul>
  </div>
</div>
