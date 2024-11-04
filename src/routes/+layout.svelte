<script>
    import "../app.css";
  
    let navItems = [
      { name: "Portfolio", href: "portfolio/" },
      { name: "About", href: "about/" },
      { name: "Contact", href: "contact/" },
    ];
  
    let isMenuOpen = false;
  
    function toggleMenu() {
      isMenuOpen = !isMenuOpen;
    }
  </script>
  
  <nav class="nav-bar">
    <div class="container mx-auto flex justify-between items-center px-4 lg:px-8">
  
      <h1 class="font-medium text-xl">
        <a href="/" class="font-bold poppins text-white hover:text-violet-400">
          Justine Jhess
        </a> 
        <span class="text-gray-300">Domenden</span> 
      </h1>  
  
  
      <div class="space-x-6 hidden md:flex">
        {#each navItems as item}
          <a href={item.href} class="nav-link text-lg hover:text-violet-400">
            {item.name}
          </a>
        {/each}
      </div>
      
  
      <div class="md:hidden">
        <button class="menu-toggle" on:click={toggleMenu} aria-label="Toggle menu">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"/>
          </svg>
        </button>
      </div>
    </div>
  
  
    {#if isMenuOpen}
      <div class="menu-items bg-gray-800 text-white md:hidden px-4 py-2 space-y-2">
        {#each navItems as item}
          <a href={item.href} class="nav-link block py-2 px-4 hover:text-violet-400">
            {item.name}
          </a>
        {/each}
      </div>
    {/if}
  </nav>
  
  <slot />
  