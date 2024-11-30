<script lang="ts">
  import type { HTMLAttributes } from "svelte/elements";
  import { cn } from "$lib/utils.js";
  import { Plus } from "lucide-svelte";

  type $$Props = HTMLAttributes<HTMLDivElement>;

  let className: $$Props["class"] = undefined;
  export { className as class };
</script>

<div
  class={cn("border bg-card text-card-foreground relative", className)}
  {...$$restProps}
>
  <Plus class="absolute h-6 w-6 -top-3 -left-3 dark:text-white text-primary" />
  <Plus
    class="absolute h-6 w-6 -bottom-3 -left-3 dark:text-white text-primary"
  />
  <Plus class="absolute h-6 w-6 -top-3 -right-3 dark:text-white text-primary" />
  <Plus
    class="absolute h-6 w-6 -bottom-3 -right-3 dark:text-white text-primary"
  />
  <slot />
</div>
