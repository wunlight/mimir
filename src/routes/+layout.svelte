<script lang="ts">
  import MenuBar from '#lib/shared/components/layout/menu-bar.svelte'
  import type { LayoutProps } from './$types'
  import './main.css'

  let { children }: LayoutProps = $props()
</script>

<div>
  <MenuBar />
  {@render children()}
</div>
