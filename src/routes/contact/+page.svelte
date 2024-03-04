<script>
  import Icon from "@iconify/svelte";

  // your script goes here
  import { MapLibre } from "svelte-maplibre";
</script>

<div class="mx-auto container p-2">
  <div class="py-2">
    <h1>Interested?</h1>
    <h2 class="font-light">Get in touch today!</h2>
  </div>

  <!-- map showing location available -->
  <!-- wrapper for padding and centering -->
  <div class="container mx-auto md:p-5">
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d208648.51845835603!2d-80.83982894999997!3d35.203153450000016!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x88541fc4fc381a81%3A0x884650e6bf43d164!2sCharlotte%2C%20NC!5e0!3m2!1sen!2sus!4v1709590417525!5m2!1sen!2sus"
      width="600"
      height="450"
      style="border:0;"
      allowfullscreen
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
      title="Area available for car repair map"
      class="border border-primary rounded-lg w-full h-96 md:h-96 map"
      >test</iframe
    >

    <div class="py-5">
      <h1>Area available for car repair</h1>
      <!--note that service is only available in Charlotte NC-->
      <h2 class="font-light">Charlotte, NC</h2>
      <p>Note: service is only available in Charlotte NC</p>
    </div>
  </div>

  <!-- row displaying phone number and hours available -->
  <div class="container mx-auto md:p-5">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
      <div class="card">
        <div class="card-body">
          <h2 class="card-title">Phone</h2>
          <p>555-555-5555</p>
        </div>
      </div>
      <div class="card">
        <div class="card-body">
          <h2 class="card-title">Hours</h2>
          <p>Date - date: #am - #pm</p>
          <p>Date: Closed</p>
        </div>
      </div>
    </div>
  </div>
  <!--on nextdoor? link to nextdoor-->
</div>
<div class="container mx-auto md:p-5">
  <div class="card">
    <div class="card-body">
      <h2 class="card-title">On Nextdoor?</h2>
      <p>Check out our reviews on Nextdoor</p>
      <!-- link  -->
      <a
        class="btn btn-primary max-w-20"
        href="https://nextdoor.com"
        target="_blank"
      >
        <Icon icon="mdi:nextdoor" />
        Nextdoor
      </a>
    </div>
  </div>
</div>

<style>
  :global(.map) {
    height: 500px;
  }
  /* default size for headers */
  h1 {
    font-size: 2.5rem;
    line-height: 1.2;
  }
  h2 {
    font-size: 2rem;
    line-height: 1.2;
  }
</style>
