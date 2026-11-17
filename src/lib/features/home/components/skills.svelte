<script>
  import Tag from '#lib/shared/components/ui/tag.svelte'
</script>

<div class="md:mx-auto px-4 md:px-8 py-6 md:py-10 xl:py-12 md:max-w-5xl xl:max-w-7xl bg-zinc-900">
  <p class="uppercase font-medium text-xl xl:text-2xl text-white">03 | Skills</p>
  <div class="grid grid-cols-2 md:grid-cols-4 xl:grid-cols-6 gap-6 mx-auto px-6 py-8 w-fit">
    <div class="relative group p-6 border-2 border-zinc-500" title="Vue.js">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <img
        src="/images/vuejs-icon.svg"
        alt="Vue.js"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
    <div class="relative group p-6 border-2 border-zinc-500" title="TypeScript">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <img
        src="/images/typescript-icon.svg"
        alt="TypeScript"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
    <div class="relative group p-6 border-2 border-zinc-500" title="Tailwind CSS">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <img
        src="/images/tailwindcss-icon.svg"
        alt="Tailwind CSS"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
    <div class="relative group p-6 border-2 border-zinc-500" title="Leaflet.js">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <img
        src="/images/leaflet-icon.svg"
        alt="Leaflet.js"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
    <div class="relative group p-6 border-2 border-zinc-500" title="Three.js">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <div class="absolute -top-3 -right-3">
        <Tag label="Exploring" variant="accent" size="sm" />
      </div>
      <img
        src="/images/threejs-icon.svg"
        alt="Three.js"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
    <div class="relative group p-6 border-2 border-zinc-500" title="PostgreSQL">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <img
        src="/images/postgres-icon.svg"
        alt="PostgreSQL"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
    <div class="relative group p-6 border-2 border-zinc-500" title="Express.js">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <img
        src="/images/express-icon.svg"
        alt="Express.js"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
    <div class="relative group p-6 border-2 border-zinc-500" title="Go">
      <div class="absolute inset-0 overflow-clip">
        <div
          class="absolute -left-1/4 -top-1/4 size-64 bg-amber-50 rounded-r-full rounded-b-full scale-0 group-hover:scale-100 transition-all duration-500 origin-top-left"
        ></div>
      </div>
      <div class="absolute -top-3 -right-3">
        <Tag label="Exploring" variant="accent" size="sm" />
      </div>
      <img
        src="/images/go-icon.svg"
        alt="Go"
        class="size-16 pointer-fine:grayscale-100 pointer-fine:group-hover:grayscale-0 group-hover:scale-110 transition-all"
      />
    </div>
  </div>
</div>
