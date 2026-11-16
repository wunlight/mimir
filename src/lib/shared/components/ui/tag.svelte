<script lang="ts">
  interface Props {
    label?: string
    icon?: string
    variant?: 'primary' | 'secondary' | 'accent' | 'outline' | 'ghost'
    size?: 'sm' | 'md' | 'lg'
  }
  let { label, icon, variant = 'primary', size = 'md' }: Props = $props()

  const variants = {
    primary: 'bg-rose-400 border-2',
    secondary: 'bg-purple-400 border-2',
    accent: 'bg-emerald-300 border-2',
    outline: 'border-2',
    ghost: 'shadow-none',
  } satisfies Record<NonNullable<Props['variant']>, string>

  const sizes = {
    sm: 'py-0.5 text-xs',
    md: 'py-1 text-sm',
    lg: 'py-3',
  } satisfies Record<NonNullable<Props['size']>, string>

  let btnClass = $derived(`${variants[variant]} ${sizes[size]}`)
</script>

<span
  class={`
    flex items-center justify-center gap-3 px-2 w-fit
    border-zinc-900 rounded-lg shadow-[4px_4px_0_0_#18181b] select-none
    ${btnClass}
  `}
>
  {#if icon}
    <span class={icon}></span>
  {/if}

  {#if label}
    <span>{label}</span>
  {/if}
</span>
