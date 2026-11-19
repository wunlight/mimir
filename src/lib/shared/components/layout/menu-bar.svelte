<script lang="ts">
  import { page } from '$app/state'
  import { fade } from 'svelte/transition'
  import Button from '../ui/button.svelte'
  import ContactDialog from './contact-dialog.svelte'

  let showMobileMenu: boolean = $state(false)

  const isActive = (path: string): boolean => page.url.pathname === path

  const navigateTo = (path: string): void => {
    showMobileMenu = false
    window.location.assign(path)
  }
</script>

<div class="menu-bar">
  <div class="block lg:hidden">
    <Button
      icon="icon-[tabler--menu-2]"
      variant="secondary"
      square
      onclick={() => (showMobileMenu = true)}
    />
  </div>
  <div class="hidden lg:flex gap-4">
    <Button
      label="Home"
      variant={isActive('/') ? 'secondary' : 'ghost'}
      onclick={() => navigateTo('/')}
    />
    <Button
      label="Projects"
      variant={isActive('/projects') ? 'secondary' : 'ghost'}
      onclick={() => navigateTo('/projects')}
    />
    <Button label="Blog" variant="ghost" disabled />
    <ContactDialog>
      {#snippet trigger(open)}
        <Button label="Contact" variant="ghost" onclick={open} />
      {/snippet}
    </ContactDialog>
    <a href="/resume.pdf" target="_blank" rel="noopener noreferrer">
      <Button label="My Resume" variant="accent" />
    </a>
  </div>
</div>

{#if showMobileMenu}
  <div
    class="fixed inset-0 z-9999 block pointer-fine:hidden bg-zinc-950/20"
    transition:fade={{ duration: 200 }}
  >
    <div class="relative flex flex-col px-4 py-6 bg-white">
      <div class="absolute right-4 top-6">
        <Button
          icon="icon-[tabler--x]"
          variant="outline"
          square
          onclick={() => (showMobileMenu = false)}
        />
      </div>

      <div class="flex flex-col items-start gap-4">
        <Button label="Home" variant="ghost" />
        <Button label="Projects" variant="ghost" disabled />
        <Button label="Blog" variant="ghost" disabled />
        <ContactDialog>
          {#snippet trigger(open)}
            <Button label="Contact" variant="ghost" onclick={open} />
          {/snippet}
        </ContactDialog>
        <a href="/resume.pdf" target="_blank" rel="noopener noreferrer">
          <Button label="My Resume" variant="ghost" />
        </a>
      </div>
    </div>
  </div>
{/if}

<style>
  .menu-bar {
    position: fixed;
    top: 1.5rem;
    right: 1rem;
    z-index: 9999;
    display: flex;
    align-items: center;
    border-radius: 0.5rem;
    transition: all 300ms ease;
  }

  @media (min-width: 80rem) {
    .menu-bar {
      right: max(0px, calc((100vw - 1200px) / 2));
    }
  }

  @media (min-width: 64rem) {
    @container scroll-state(scrollable: top) {
      .menu-bar {
        padding: 1rem;
        background-color: var(--color-zinc-50);
        border: 3px solid var(--color-zinc-900);
        box-shadow: var(--shadow-lg);
      }
    }
  }
</style>
