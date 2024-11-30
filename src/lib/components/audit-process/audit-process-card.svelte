<script lang="ts">
  import CardContent from "../ui/card/card-content.svelte";
  import Card from "../ui/card/card.svelte";

  type $$Props = {
    title: string;
    description: string;
    illustration: string;
  };
  let { title, description, illustration }: $$Props = $props();
</script>

<Card class="h-full px-5 py-16">
  <CardContent class="flex h-full items-start justify-between gap-4">
    <img
      height={84}
      width={84}
      src={illustration}
      alt="Audit Process Illustration"
      class="!m-0"
    />
    <div>
      <p class="text-2xl font-semibold">{title}</p>
      <p class="text-base font-normal">{description}</p>
    </div>
  </CardContent>
</Card>
