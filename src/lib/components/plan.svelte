<script>
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
          class="bg-[#FF8C02] cursor-pointer w-11/12 m-auto text-white rounded-md p-3 text-sm font-light mt-8 text-center block"
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
