<script>
  import ContactDialog from '#lib/shared/components/layout/contact-dialog.svelte'
  import Button from '#lib/shared/components/ui/button.svelte'
</script>

<div
  class="grid grid-cols-1 md:grid-cols-2 md:mx-auto md:max-w-5xl xl:max-w-7xl border-x-4 border-t-4 border-zinc-900 md:divide-x-4 divide-y-4 md:divide-y-0 divide-zinc-900"
  style="border-top-style: dashed"
>
  <div class="px-12 py-6 flex flex-col h-full bg-purple-700">
    <p class="uppercase font-medium text-xl xl:text-2xl text-white">02 | Services</p>
    <div class="flex flex-col gap-6 my-auto">
      <div class="space-y-1.5">
        <p class="font-bold text-4xl text-white">Web Application Development</p>
        <p class="text-zinc-200">
          Developing functional web applications tailored to specific business needs.
        </p>
      </div>
      <div class="flex gap-4">
        <ContactDialog>
          {#snippet trigger(open)}
            <Button label="Let's Talk" icon="icon-[tabler--phone]" variant="warn" onclick={open} />
          {/snippet}
        </ContactDialog>
        <Button
          label="Learn More"
          icon="icon-[tabler--arrow-up-right] text-2xl"
          iconPos="right"
          variant="accent"
          disabled
        />
      </div>
    </div>
  </div>
  <div class="flex flex-col divide-y-4 divide-zinc-900">
    <div class="flex flex-col gap-6 px-12 py-10 bg-emerald-200">
      <div class="space-y-1.5">
        <p class="font-bold text-4xl">Website Development</p>
        <p class="text-zinc-700">
          Building modern websites that help businesses and individuals establish their digital
          presence.
        </p>
      </div>
      <div>
        <Button
          label="Learn More"
          icon="icon-[tabler--arrow-up-right] text-2xl"
          iconPos="right"
          disabled
        />
      </div>
    </div>
    <div class="flex flex-col gap-6 px-12 py-10 bg-white">
      <div class="space-y-1.5">
        <p class="font-bold text-4xl">CMS Integration & Development</p>
        <p class="text-zinc-500">
          Integrating content management systems that make website content easier to manage and
          update.
        </p>
      </div>
      <div>
        <Button
          label="Learn More"
          icon="icon-[tabler--arrow-up-right] text-2xl"
          iconPos="right"
          variant="secondary"
          disabled
        />
      </div>
    </div>
  </div>
</div>
