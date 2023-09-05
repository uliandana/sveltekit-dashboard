<script lang="ts">
  import '../app.css';
  import { page } from '$app/stores';
  import imgLogo from '$lib/assets/logo.svg';
  import icBell from '$lib/assets/bell.svg';
  import icSearch from '$lib/assets/search.svg';
  import icCog from '$lib/assets/cog.svg';
  import icUserCircle from '$lib/assets/user-circle.svg';
  import icNavTables from '$lib/assets/nav-tables.svg';

  $: pathname = $page.url.pathname;

  $: navClass = (href: string) => {
    const c = 'w-[13.6875rem] flex items-center gap-[0.75rem] px-[1rem] py-[0.75rem] text-[0.875rem]';
    return pathname === href ? `${c} bg-white rounded` : c;
  };
</script>

<div class="app-grid bg-[#F8F9FA] text-[#67748E] min-h-screen">
  <aside class="flex flex-col p-[2rem]">
    <img class="w-[10.375rem]" alt="Logo" src={imgLogo} />
    <nav class="flex flex-col mt-[2rem]">
      {#each [
        { icon: icNavTables, text: 'Dashboard', href: '/' },
        { icon: icNavTables, text: 'Tables', href: '/tables' },
        { icon: icNavTables, text: 'Billing', href: '/billing' },
        { icon: icNavTables, text: 'RTL', href: '/rtl' },
      ] as l}
        <a href={l.href} class={navClass(l.href)}>
          <img alt="icon" class="w-[2rem] shadow-md" src={l.icon} />
          {l.text}
        </a>
      {/each}
      <h3 class="my-[1rem] text-[0.8125rem] font-[700] uppercase">Account Pages</h3>
      {#each [
        { icon: icNavTables, text: 'Profile', href: '/profile' },
        { icon: icNavTables, text: 'Sign In', href: '/sign-in' },
        { icon: icNavTables, text: 'Sign Up', href: '/sign-up' },
      ] as l}
        <a href={l.href} class={navClass(l.href)}>
          <img alt="icon" class="w-[2rem] shadow-md" src={l.icon} />
          {l.text}
        </a>
      {/each}
    </nav>
  </aside>
  <header class="flex items-center justify-between py-[1.25rem]">
    <div>
      <p class="text-[0.875rem] mb-[0.25rem]">
        Pages / <span class="text-[#252F40]">Dashboard</span>
      </p>
      <h2 class="text-[1rem] text-[#252F40] font-[700]">Dashboard</h2>
    </div>
    <div class="flex justify-end items-center gap-[1rem] mr-[2rem]">
      <div class="flex items-center gap-[0.5rem] bg-[#FFF] border-[#D2D6DA]">
        <img alt="icon search" src={icSearch} />
        <input placeholder="Type here..." />
      </div>
      <a href="/sign-in" class="flex items-center gap-[0.25rem]">
        <img alt="icon user" src={icUserCircle} />
        <span>Sign In</span>
      </a>
      <img alt="icon cog" src={icCog} />
      <img alt="icon bell" src={icBell} />
    </div>
  </header>
  <main>
    <slot />
  </main>
  <footer class="flex justify-between py-[1.25rem]">
    <p>
      &copy; 2021, made by <strong>Creative Tim</strong> for a better web.
    </p>
    <ul class="flex items-center gap-[2rem] mr-[2rem]">
      <li>Creative Tim</li>
      <li>About Us</li>
      <li>Blog</li>
      <li>License</li>
    </ul>
  </footer>
</div>

<style>
  .app-grid {
    display: grid;
    grid-template-columns: auto 1fr;
    grid-template-rows: auto 1fr auto;
  }
  .app-grid > aside {
    grid-column: 1;
    grid-row: 1/4;
  }
  .app-grid > header {
    grid-column: 2;
    grid-row: 1;
  }
  .app-grid > main {
    grid-column: 2;
    grid-row: 2;
  }
  .app-grid > footer {
    grid-column: 2;
    grid-row: 3;
  }
</style>
