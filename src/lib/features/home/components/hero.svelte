<script lang="ts">
  import Tag from '#lib/shared/components/ui/tag.svelte'
</script>

<div
  class="flex flex-col gap-3 md:mx-auto px-4 md:px-8 py-6 md:py-10 xl:py-12 md:max-w-5xl xl:max-w-7xl bg-amber-100 border-x-4 border-zinc-900"
>
  <div class="space-y-0">
    <p class="uppercase font-medium text-6xl xl:text-8xl">Hello,</p>
    <p class="uppercase font-medium text-6xl xl:text-8xl">I Am Rafael</p>
  </div>
  <div class="flex px-2 gap-3">
    <span class="icon-[tabler--arrow-loop-left] size-8 rotate-190"></span>
    <Tag label="Frontend Engineer" variant="secondary" />
  </div>
  <div class="flex flex-col gap-1.5 ml-auto mt-16 max-w-64 xl:max-w-72">
    <div class="self-end h-1.5 w-20 bg-zinc-900"></div>
    <p class="text-right">
      Focused on solving problems and turning ideas into functional, well-crafted web applications.
    </p>
    <div class="self-center h-1.5 w-20 bg-zinc-900"></div>
  </div>
</div>
