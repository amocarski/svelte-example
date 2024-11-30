<script lang="ts">
  import Container from "$lib/components/ui/container/container.svelte";
  import Section from "$lib/components/ui/section/section.svelte";
  import Header from "../ui/header/header.svelte";
  import ServiceCard from "./service-card.svelte";
</script>

<Section>
  <Container>
    <Header
      subHeading="Let us help securing your product"
      title="OUR SERViCES"
    />
    <div class="flex flex-col gap-6 mt-10">
      <div class="grid grid-cols-12 gap-6">
        <div class="col-span-full md:col-span-7">
          <ServiceCard
            title="Smart Contract Audits"
            description="Secure and optimize your smart contracts with expert precision from start to finish."
          />
        </div>
        <div class="col-span-full md:col-span-5">
          <ServiceCard
            title="Security Advisory"
            description="Get guidance and help from technical design to the deployment."
          />
        </div>
      </div>

      <div class="grid grid-cols-12 gap-6">
        <div class="col-span-full md:col-span-5">
          <ServiceCard
            title="Fuzzing and Invariants"
            description="Bootstrap fuzzing and invariant tests for your projects with us."
          />
        </div>
        <div class="col-span-full md:col-span-7">
          <ServiceCard
            title="Off-chain Components Verification"
            description="Ensure your off-chain components are secure with rigorous web, mobile, and cloud security testing."
          />
        </div>
      </div>
    </div>
  </Container>
</Section>
