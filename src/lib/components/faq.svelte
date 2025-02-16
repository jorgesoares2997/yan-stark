<script lang="ts">
  interface FAQItem {
    question: string;
    answer: string;
  }
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
</script>

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
            class={`min-w-5 max-w-5 max-h-5 min-h-5 transform transition-transform duration-300 ease-in-out ${activeQuestion === question ? "rotate-180" : ""}`}
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
