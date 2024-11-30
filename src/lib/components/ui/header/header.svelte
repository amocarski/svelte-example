<script lang="ts">
  import type { Snippet } from "svelte";
  import type { HTMLAttributes } from "svelte/elements";
  import HeadingPointer from "../heading-pointer.svelte";

  type $$Props = HTMLAttributes<HTMLDivElement> & {
    title: string;
    subHeading?: string | number;
    children?: Snippet;
  };
  let { title, subHeading, children }: $$Props = $props();
</script>

<div class="w-fit">
  {#if subHeading}
    <p class="text-muted-foreground ml-11 text-lg font-medium">
      {subHeading}
    </p>
  {/if}
  <div class="flex items-center gap-3">
    <HeadingPointer />
    <h2 class="text-primary !m-0 !font-mono !text-4xl md:!text-5xl">
      {title}
    </h2>
  </div>
  {#if children}
    <div class="text-base font-light">
      {@render children?.()}
    </div>
  {/if}
</div>
