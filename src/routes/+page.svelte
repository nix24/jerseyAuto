<!-- 
    https://computer-repair-128.webflow.io/
    https://eurofitautocentres.co.uk/
 -->
<script>
  import { reveal } from "svelte-reveal";
  import Icon from "@iconify/svelte";
  import kiaSorentoFront from "../assets/kiaSorentoFront.jpg";
  let placeholders = new Array(6).fill(null).map(() => {
    const width = Math.floor(Math.random() * (500 - 200 + 1)) + 200;
    const height = Math.floor(Math.random() * (500 - 200 + 1)) + 200;
    return `https://via.placeholder.com/${width}x${height}`;
  });
</script>

<section use:reveal={{ transition: "fly", delay: 200 }} id="hero">
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row-reverse">
      <img
        src="https://placeholder.com/600x400"
        class="max-w rounded-lg shadow-2xl"
        alt="car"
      />
      <div class="text-center lg:text-left">
        <h1 class="text-5xl font-bold">
          Quality Car Repairs by an Expert Mechanic
        </h1>
        <p class="py-6">
          Get your car back on the road with our reliable and affordable repair
          services
        </p>
        <a href="/contact" class="btn btn-primary">Get in Contact</a>
      </div>
    </div>
  </div>
</section>

<section
  id="about"
  class="container mx-auto py-8 grid md:grid-cols-3 grid-cols-1 items-center justify-center mb-32"
>
  <div class="card" use:reveal={{ transition: "slide", delay: 200 }}>
    <figure class="avatar p-5">
      <div
        class="w-60 rounded-full ring ring-primary ring-offset-base-100 ring-offset-4"
      >
        <img src="https://placeholder.com/600x400" alt="Car Repair Service" />
      </div>
    </figure>
    <div class="card-body items-center text-center">
      <h2 class="card-title">Experienced Repair <Icon icon="mdi:car" /></h2>
      <p>
        you need someone who has the knowledge and skills to handle any car
        repair.
      </p>
      <div class="card-actions"></div>
    </div>
  </div>
  <div class="card" use:reveal={{ transition: "slide", delay: 200 }}>
    <figure class="avatar p-5">
      <div
        class="w-60 rounded-full ring ring-primary ring-offset-base-100 ring-offset-4"
      >
        <img src="https://placeholder.com/600x400" alt="Car Repair Service" />
      </div>
    </figure>
    <div class="card-body items-center text-center">
      <h2 class="card-title">Affordable Pricing <Icon icon="ph:money" /></h2>
      <p>
        I offer affordable solutions for all types of car repairs, ensuring that
        you can get your vehicle back on the road without breaking the bank.
      </p>
      <div class="card-actions"></div>
    </div>
  </div>
  <div class="card" use:reveal={{ transition: "slide", delay: 200 }}>
    <figure class="avatar p-5">
      <div
        class="w-60 rounded-full ring ring-primary ring-offset-base-100 ring-offset-4"
      >
        <img src="https://placeholder.com/600x400" alt="Car Repair Service" />
      </div>
    </figure>
    <div class="card-body items-center text-center">
      <h2 class="card-title">Quick Turnaround <Icon icon="ph:clock" /></h2>
      <p>
        I strive to provide fast and efficient car repairs to get you back on
        the road in no time.
      </p>
    </div>
  </div>
  <div class="md:col-span-3 flex justify-center items-center">
    <a href="/contact" class="btn btn-primary">Get in Contact</a>
  </div>
</section>
<div class="pb-20 mb-20">
  <section id="services" class="container mx-auto px-5 py-8">
    <!-- content -->
    <div class="=relative bg-base-200 rounded-t-3xl overflow-hidden">
      <!-- image -->
      <div
        class="hero min-h-screen"
        style={`background-image: url(${kiaSorentoFront});`}
      >
        <div class="hero-overlay bg-opacity-60"></div>
        <div class="hero-content text-center text-neutral-content">
          <div use:reveal={{ transition: "blur", delay: 200 }}>
            <h1 class="mb-5 text-5xl font-bold">Fast, Reliable, Cheap</h1>
            <p class="mb-5">
              Provident cupiditate voluptatem et in. Quaerat fugiat ut assumenda
              excepturi exercitationem quasi. In deleniti eaque aut repudiandae
              et a id nisi.
            </p>
          </div>
        </div>
      </div>
      <div class="container mx-auto p-5 pt-20 md:pt-24">
        <div
          use:reveal={{ transition: "fade", delay: 200 }}
          class="pt-20 md:pt-0 grid grid-cols-1 md:grid-cols-2 gap-4 items-center h-full"
        >
          <div class="space-y-4">
            <h1 class="font-bold">Services</h1>
            <h2 class="font-semibold">
              I fix engines, wheels, spark plugs, and more
            </h2>
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eligendi
              alias impedit praesentium veniam cumque eos libero laboriosam
              suscipit tempore? Beatae eos iste debitis quae autem alias qui
              dolores perspiciatis id.
            </p>
          </div>
          <div
            use:reveal={{ transition: "slide" }}
            class="stats stats-vertical shadow"
          >
            <div class="stat">
              <div class="stat-title font-semibold text-xl">
                Vehicles Repaired
              </div>
              <div class="stat-value">100+</div>
              <div class="stat-desc">Reliable and Trusted Service</div>
            </div>

            <div class="stat">
              <div class="stat-title font-semibold text-xl">
                Years of Experience
              </div>
              <div class="stat-value">10+</div>
              <div class="stat-desc">Only Quality & Dedication</div>
            </div>

            <div class="stat">
              <div class="stat-title font-semibold text-xl">Satisfaction</div>
              <div class="stat-value">98%</div>
              <div class="stat-desc">No Customer left unsatisfied</div>
            </div>

            <div class="stat">
              <div class="stat-title font-semibold text-xl">
                Services Offered
              </div>
              <div class="stat-value">15+</div>
              <div class="stat-desc">Full Range of Repairs</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>

<section id="reviews" class="container mx-auto py-8">
  <h2 class="text-2xl font-bold mb-4">Customer Reviews</h2>
  <div class="flex flex-col space-y-5">
    <article
      class="border border-accent rounded-lg flex flex-row p-4 shadow-lg"
    >
      <div class="avatar">
        <div class="w-24 rounded-full">
          <img
            src="https://daisyui.com/images/stock/photo-1534528741775-53994a69daeb.jpg"
            alt="reviewImg"
            class="mask mask-squircle"
          />
        </div>
      </div>
      <blockquote class="flex flex-col justify-center ml-4">
        <cite class="text-lg font-semibold">John Doe</cite>
        <p class="text-sm text-accent italic">
          "This product has been a game-changer for me. Highly recommend trying
          it out!"
        </p>
      </blockquote>
    </article>
    <article
      class="border border-accent rounded-lg flex flex-row p-4 shadow-lg"
    >
      <div class="avatar">
        <div class="w-24 rounded-full">
          <img
            src="https://daisyui.com/images/stock/photo-1534528741775-53994a69daeb.jpg"
            alt="reviewImg"
            class="mask mask-squircle"
          />
        </div>
      </div>
      <blockquote class="flex flex-col justify-center ml-4">
        <cite class="text-lg font-semibold">John Doe</cite>
        <p class="text-sm text-accent italic">
          "This product has been a game-changer for me. Highly recommend trying
          it out!"
        </p>
      </blockquote>
    </article>
  </div>
</section>

<section id="gallery" class="container mx-auto py-8">
  <h2 class="text-2xl font-bold mb-4">Car Repairs Gallery</h2>
  <p class="mb-4">Browse our collection of previous successful car repairs.</p>
  <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
    <!-- Dynamically create columns with Svelte {#each} blocks -->
    {#each Array(4) as _, colIndex}
      <div class="grid gap-4">
        {#each placeholders as placeholder, i}
          {#if i % 4 === colIndex}
            <div>
              <img
                class="h-auto max-w-full rounded-lg"
                src={placeholder}
                alt={`Placeholder ${i}`}
              />
            </div>
          {/if}
        {/each}
      </div>
    {/each}
  </div>
</section>

<style>
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
