<script>
  import { homePageConfig } from "../../../config/home-page";
  import Button from "../ui/button/button.svelte";
  import Container from "../ui/container/container.svelte";
  import Header from "../ui/header/header.svelte";

  import Section from "../ui/section/section.svelte";
  import AuditProcessCard from "./audit-process-card.svelte";
</script>

<Section class="bg-background relative z-30 !py-20" id="process">
  <Container>
    <div class="flex flex-col items-start gap-6 md:flex-row">
      <Header
        subHeading="Security Audits"
        title="AUdit PrOCess"
        class="top-0 mb-10 pt-6 md:sticky"
      >
        <div class="flex flex-col items-start gap-6">
          Our audit process takes you from defining clear goals through
          meticulous code analysis and dynamic testing, and finishes with a
          thorough review and detailed reporting to ensure your protocol is both
          secure and spotlight-ready.
          <Button>Check Out Our Public Audits</Button>
        </div>
      </Header>
      <div class="flex w-full flex-col gap-6 pt-6">
        {#each homePageConfig.auditProcess as item}
          <AuditProcessCard {...item} />
        {/each}
      </div>
    </div>
  </Container>
</Section>
