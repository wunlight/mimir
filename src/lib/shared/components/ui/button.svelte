<script lang="ts">
  interface Props {
    label?: string
    icon?: string
    iconPos?: 'left' | 'right'
    variant?: 'primary' | 'secondary' | 'accent' | 'warn' | 'outline' | 'ghost'
    size?: 'sm' | 'md' | 'lg'
    square?: boolean
    disabled?: boolean
    onclick?: (e: MouseEvent) => void
  }
  let {
    label,
    icon,
    iconPos = 'left',
    variant = 'primary',
    size = 'md',
    square = false,
    disabled = false,
    onclick,
  }: Props = $props()

  const variants = {
    primary: 'bg-rose-400 hover:bg-rose-500 border-2',
    secondary: 'bg-purple-400 hover:bg-purple-500 border-2',
    accent: 'bg-emerald-300 hover:bg-emerald-400 border-2',
    warn: 'bg-amber-400 hover:bg-amber-500 border-2',
    outline: 'border-2',
    ghost: 'hover:bg-zinc-900/10 shadow-none',
  } satisfies Record<NonNullable<Props['variant']>, string>

  const sizes = {
    sm: 'h-8.5 text-sm',
    md: 'h-11 text-base',
    lg: 'h-12 text-lg',
  } satisfies Record<NonNullable<Props['size']>, string>

  let btnClass = $derived(
    `${variants[variant]} ${sizes[size]} ${iconPos === 'right' ? 'flex-row-reverse' : 'flex-row'} ${square ? 'aspect-square' : 'px-3'}`,
  )
</script>

<button
  class={`
    flex items-center justify-center gap-3
    border-zinc-900 rounded-lg shadow-[4px_4px_0_0_#18181b]
    transition-all select-none
    disabled:opacity-50 disabled:pointer-events-none
    active:scale-95
    not-disabled:cursor-pointer
    ${btnClass}
  `}
  {disabled}
  {onclick}
>
  {#if icon}
    <span class={icon}></span>
  {/if}

  {#if label}
    <span>{label}</span>
  {/if}
</button>
