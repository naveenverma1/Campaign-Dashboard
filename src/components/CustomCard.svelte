<script>
  import Card from "sveltestrap/src/Card.svelte";
  import CardBody from "sveltestrap/src/CardBody.svelte";
  import CardHeader from "sveltestrap/src/CardHeader.svelte";



  export let cardTitle = "dwefdef";
  export let cardIcon = "dwwwwwwwwe";
</script>

<Card class="mb-4">
  <CardHeader>
    <i class={cardIcon} />
    {cardTitle}
  </CardHeader>
  <CardBody>
    <slot />
    <slot name="chartCaption" />
  </CardBody>
</Card>
