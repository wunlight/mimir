<script lang="ts">
  interface Props {
    label?: string
    disabled?: boolean
  }
  let { label, disabled = false }: Props = $props()
</script>

<label class={`flex gap-3 ${disabled ? 'opacity-80' : ''}`}>
  <input
    type="checkbox"
    class="
      appearance-none size-5 shrink-0 border-2 rounded-sm
      not-disabled:cursor-pointer disabled:pointer-events-none
      border-zinc-900 shadow-[2px_2px_0_0_#18181b]
      checked:bg-rose-500 checked:before:content-['✓']
      checked:before:grid checked:before:place-content-center
      checked:before:size-4 checked:before:text-white checked:before:font-bold
      focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-rose-500
    "
    {disabled}
  />
  <span class="select-none">{label}</span>
</label>
