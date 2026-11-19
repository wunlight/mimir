<script>
  import Button from '#lib/shared/components/ui/button.svelte'
</script>

<div
  class="md:mx-auto px-4 md:px-8 py-6 md:py-10 xl:py-12 md:max-w-5xl xl:max-w-7xl bg-zinc-800 border-x-4 border-zinc-900"
>
  <p class="uppercase font-medium text-xl xl:text-2xl text-white">02 | Featured</p>
  <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-6 px-6 py-8">
    <div class="flex flex-col">
      <div
        class="bg-zinc-50 border-4 border-zinc-900 rounded-lg shadow-[4px_4px_0_0_#ec003f,9px_9px_0_0_#18181b]"
      >
        <img
          src="/images/amigo-thumbnail.jpg"
          alt="amigo dashboard"
          class="size-full object-cover rounded-sm"
        />
      </div>
      <div class="flex flex-col pt-5 pb-3">
        <h2 class="font-medium text-2xl text-zinc-50 truncate">Amigo Workshop - POS</h2>
        <p class="line-clamp-3 text-zinc-300">
          A workshop management system built with Vue.js and Go, featuring spare parts inventory
          management, transaction processing, and sales performance reporting.
        </p>
      </div>
      <div class="flex gap-3">
        <Button label="Read More" variant="secondary" disabled />
      </div>
    </div>

    <div class="flex flex-col">
      <div
        class="bg-zinc-50 border-4 border-zinc-900 rounded-lg shadow-[4px_4px_0_0_#fcc800,9px_9px_0_0_#18181b]"
      >
        <img
          src="/images/heimdall-thumbnail.jpg"
          alt="heimdall prototype"
          class="size-full object-cover rounded-sm"
        />
      </div>
      <div class="flex flex-col pt-5 pb-3">
        <h2 class="font-medium text-2xl text-zinc-50 truncate">
          Heimdall - Spatial Emergency Monitoring Prototype
        </h2>
        <p class="line-clamp-3 text-zinc-300">
          An emergency fire monitoring prototype built with Vue.js, Three.js, and Leaflet.js,
          designed to visualize building layouts, monitor device statuses, and replay emergency
          incidents across multiple floors.
        </p>
      </div>
      <div class="flex gap-3">
        <Button label="View Prototype" variant="accent" disabled />
        <Button label="Read More" variant="secondary" disabled />
      </div>
    </div>

    <!-- <div class="flex flex-col">
      <div
        class="bg-zinc-50 border-4 border-zinc-900 rounded-lg shadow-[4px_4px_0_0_#00a63e,9px_9px_0_0_#18181b]"
      >
        <img
          src="/images/amigo-thumbnail.jpg"
          alt="amigo dashboard"
          class="size-full object-cover rounded-sm"
        />
      </div>
      <div class="flex flex-col pt-5 pb-3">
        <h2 class="font-medium text-2xl text-zinc-50 truncate">
          Headline - If Have Very Long Headline
        </h2>
        <p class="line-clamp-3 text-zinc-300">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae deleniti optio ad, nulla
          nam nisi perspiciatis nobis accusantium exercitationem cum commodi unde eius iure ea
          recusandae maiores magnam. Impedit, enim!
        </p>
      </div>
    </div> -->
  </div>
</div>
