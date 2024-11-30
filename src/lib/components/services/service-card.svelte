<script lang="ts">
  import type { HTMLAttributes } from "svelte/elements";
  import { cn } from "$lib/utils.js";
  import { Card, CardContent } from "../ui/card";

  type $$Props = HTMLAttributes<HTMLDivElement> & {
    title: string;
    description: string;
  };

  let { title, description }: $$Props = $props();
  let className = $state<$$Props["class"]>(undefined);
  export { className as class };
</script>

<div
  class={cn(
    "bg-card text-card-foreground rounded-lg border shadow-sm",
    className
  )}
>
  <Card class="h-full px-8 py-40">
    <CardContent class="flex h-full flex-col justify-between">
      <p class="text-2xl font-semibold">{title}</p>
      <p class="text-base font-normal">{description}</p>
    </CardContent>
  </Card>
</div>
