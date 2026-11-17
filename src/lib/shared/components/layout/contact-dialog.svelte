<script lang="ts">
  import type { Snippet } from 'svelte'
  import { fade } from 'svelte/transition'
  import Button from '../ui/button.svelte'

  let {
    trigger,
  }: {
    trigger: Snippet<[() => void]>
  } = $props()

  let isOpen = $state(false)
</script>

{@render trigger(() => (isOpen = true))}

{#if isOpen}
  <div
    class="fixed inset-0 z-9999 grid place-content-center bg-zinc-950/20 backdrop-blur"
    transition:fade={{ duration: 200 }}
  >
    <div class="flex flex-col gap-1.5 p-4 bg-white rounded-lg">
      <div class="flex items-center justify-between gap-8">
        <p class="font-medium text-xl">My Contacts</p>
        <Button
          icon="icon-[tabler--x]"
          variant="ghost"
          square
          size="sm"
          onclick={() => (isOpen = false)}
        />
      </div>
      <hr class="border-zinc-300" />
      <div class="flex flex-col gap-3 py-3">
        <a href="mailto:rafael14wun@gmail.com" class="flex items-center gap-3 hover:text-blue-500">
          <span class="icon-[tabler--mail] shrink-0 size-6"></span>
          <span>rafael14wun@gmail.com</span>
        </a>

        <a
          href="https://www.linkedin.com/in/rafael-wun-4411243a3"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center gap-3 hover:text-blue-500"
        >
          <span class="icon-[tabler--brand-linkedin] shrink-0 size-6"></span>
          <span>linkedin.com/in/rafael-wun-4411243a3</span>
        </a>

        <a
          href="https://github.com/wunlight"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center gap-3 hover:text-blue-500"
        >
          <span class="icon-[tabler--brand-github] shrink-0 size-6"></span>
          <span>github.com/wunlight</span>
        </a>
      </div>
    </div>
  </div>
{/if}
