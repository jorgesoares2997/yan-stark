<script>
  let links = [
    { name: "Início", href: "#inicio" },
    { name: "Sobre", href: "#sobre" },
    { name: "Professor", href: "#teacher" },
    { name: "Plano", href: "#plano" },
    { name: "FAQ", href: "#faq" },
  ];

  /**
   * @param {MouseEvent & { currentTarget: EventTarget & HTMLAnchorElement; }} event
   * @param {string} href
   */
  function scrollToSection(event, href) {
    event.preventDefault();
    const section = document.querySelector(href);
    if (section) {
      section.scrollIntoView({ behavior: "smooth", block: "start" });
    }
  }
</script>

<nav class="bg-black text-white h-16 p-4 shadow-lg fixed top-0 left-0 w-full z-50 flex justify-between items-center">
  <a href="/" class="text-2xl hidden lg:flex font-bold">Yan Stark</a>
  <ul class="flex space-x-6 lg:w-1/3 w-full justify-between text-right">
    {#each links as link}
      <li>
        <a
          href={link.href}
          class="hover:underline cursor-pointer whitespace-nowrap"
          on:click={(event) => scrollToSection(event, link.href)}
        >
          {link.name}
        </a>
      </li>
    {/each}
  </ul>
</nav>