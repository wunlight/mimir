<script lang="ts">
  import MenuBar from '#lib/shared/components/layout/menu-bar.svelte'
  import type { LayoutProps } from './$types'
  import './main.css'

  let { children }: LayoutProps = $props()
</script>

<main class="default-layout">
  <MenuBar />

  {@render children()}

  <button
    class="back-to-top"
    aria-label="Back to top"
    onclick={() =>
      window.scrollTo({
        top: 0,
        behavior: 'smooth',
      })}
  >
    <span class="icon-[tabler--arrow-up] text-xl"></span>
  </button>
</main>

<style>
  .back-to-top {
    position: fixed;
    right: 1.5rem;
    bottom: 1.5rem;
    z-index: 9998;
    display: grid;
    place-items: center;
    width: 2.75rem;
    height: 2.75rem;
    border: 2px solid var(--color-zinc-900);
    border-radius: 0.5rem;
    background-color: var(--color-blue-400);
    color: var(--color-zinc-50);
    box-shadow: 4px 4px 0 0 var(--tw-shadow-color, #18181b);
    cursor: pointer;
    opacity: 0;
    visibility: hidden;
    transform: translateY(1rem);
    transition: all 200ms ease;
  }

  .back-to-top:hover {
    background-color: var(--color-blue-500);
    transform: translateY(-2px);
  }

  @container scroll-state(scrollable: top) {
    .back-to-top {
      opacity: 1;
      visibility: visible;
      transform: translateY(0);
    }
  }
</style>
