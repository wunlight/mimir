<script lang="ts">
  import { fade } from 'svelte/transition'
  import Button from '../ui/button.svelte'

  let showMobileMenu: boolean = $state(false)
  let isScrolled: boolean = $state(false)

  function handleScroll() {
    isScrolled = window.scrollY > 0
  }
</script>

<svelte:window onscroll={handleScroll} />

<div
  class="fixed right-4 xl:right-[max(0px,calc((100vw-1200px)/2))] top-6 flex items-center p-4 rounded-lg transition-all duration-300"
  class:bg-amber-200={isScrolled}
  class:shadow={isScrolled}
>
  <div class="block lg:hidden">
    <Button
      icon="icon-[tabler--menu-2]"
      variant="secondary"
      square
      onclick={() => (showMobileMenu = true)}
    />
  </div>
  <div class="hidden lg:flex gap-4">
    <Button label="Home" variant="ghost" />
    <Button label="Projects" variant="ghost" />
    <Button label="Blog" variant="ghost" />
    <Button label="Contact" variant="ghost" />
    <Button label="My Resume" variant="accent" />
  </div>
</div>

{#if showMobileMenu}
  <div class="fixed inset-0 z-9999 bg-zinc-950/20" transition:fade={{ duration: 200 }}>
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
        <Button label="Projects" variant="ghost" />
        <Button label="Blog" variant="ghost" />
        <Button label="Contact" variant="ghost" />
        <Button label="My Resume" variant="accent" />
      </div>
    </div>
  </div>
{/if}
