// @ts-ignore
<script lang="ts">
  import { page } from "$app/stores"
  import '../styles/app.css';
</script>

<div class="app">
  <header>
    <nav>
      <ul>
        <!-- ここで設定している `aria-current` とはなんでしょう？是非調べてみてください！ -->
        <li class="nav-item" aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
          <a href="/">Home</a>
        </li>
        <li class="nav-item" aria-current={$page.url.pathname === '/cats' ? 'page' : undefined}>
          <a href="/cats">Cats</a>
        </li>
        
      </ul>
    </nav>
  </header>

  <main>
    <slot />
  </main>

  <footer>
    SvelteKit hands-on de tsukurimashita &copy;
  </footer>
</div>

<style>
</style>
