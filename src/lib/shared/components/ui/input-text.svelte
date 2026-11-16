<script lang="ts">
  interface Props {
    placeholder?: string
    prefixIcon?: string
    suffixIcon?: string
    invalid?: boolean
    disabled?: boolean
  }
  let { placeholder, prefixIcon, suffixIcon, invalid, disabled }: Props = $props()

  let inputClass = $derived(
    `${invalid ? 'border-red-500 shadow-[4px_4px_0_0_#ef4444]' : 'border-zinc-900 shadow-[4px_4px_0_0_#18181b]'}`,
  )
</script>

<div
  class={`
    flex items-center gap-3
    px-3 h-11
    border-2 rounded-lg
    disabled:opacity-80
    ${inputClass}
  `}
>
  {#if prefixIcon}
    <span class={prefixIcon}></span>
  {/if}

  <input {placeholder} {disabled} class="outline-none" />

  {#if suffixIcon}
    <span class={suffixIcon}></span>
  {/if}
</div>
