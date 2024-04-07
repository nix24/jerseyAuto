<!-- 
    https://computer-repair-128.webflow.io/
    https://eurofitautocentres.co.uk/
 -->
<script>
  import { reveal } from "svelte-reveal";
  import Icon from "@iconify/svelte";
  import kiaSorentoFront from "$lib/assets/kiaSorentoFront.jpg";
  import ContactBtn from "$lib/components/contactBtn.svelte";
  import galleryImg1 from "$lib/assets/galleryImg1.jpg";
  import galleryImg2 from "$lib/assets/galleryImg2.jpg";
  import galleryImg3 from "$lib/assets/galleryImg3.jpg";
  import galleryImg4 from "$lib/assets/galleryImg4.jpg";
  import galleryImg5 from "$lib/assets/galleryImg5.jpg";

  let galleryImages = [
    galleryImg1,
    galleryImg2,
    galleryImg3,
    galleryImg4,
    galleryImg5,
  ];
</script>

<section id="hero">
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row-reverse">
      <enhanced:img
        src="../lib/assets/heroImg.jpg"
        class="max-w rounded-lg shadow-2xl"
        alt="heroImg"
        sizes="(max-width: 768px) 100vw, 50vw"
      />
      <div
        use:reveal={{ transition: "fly", delay: 200 }}
        class="text-pretty lg:text-left md:w-1/2 p-5"
      >
        <h1 class="text-5xl font-bold">
          <span class="iconify mr-2" data-icon="mdi:car-wrench"></span>
          Expert Mobile Auto Mechanic Services
        </h1>
        <p class="py-6">
          From brakes and rotors to tune-ups and oil changes, I treat every
          vehicle as if it were my own. I offer the convenience and reliability
          that you deserve with your vehicle.
        </p>
        <ContactBtn />
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
        <enhanced:img
          src="../lib/assets/galleryImg8.jpg"
          alt="Experienced Mechanic"
          sizes="(max-width: 768px) 100vw, 50vw"
        />
      </div>
    </figure>
    <div class="card-body items-center text-center">
      <h2 class="card-title">
        Experienced Mechanic <Icon icon="mdi:car-wrench" />
      </h2>
      <p>
        With years of experience in the automotive industry, you need somone who
        has the knowledge and skills to handle any car repair.
      </p>
    </div>
  </div>

  <div class="card" use:reveal={{ transition: "slide", delay: 200 }}>
    <figure class="avatar p-5">
      <div
        class="w-60 rounded-full ring ring-primary ring-offset-base-100 ring-offset-4"
      >
        <enhanced:img
          src="../lib/assets/galleryImg7.jpg"
          alt="Affordable Pricing"
          sizes="(max-width: 768px) 100vw, 50vw"
        />
      </div>
    </figure>
    <div class="card-body items-center text-center">
      <h2 class="card-title">Affordable Pricing <Icon icon="ph:money" /></h2>
      <p>
        I believe in providing quality car repair services at competitive
        prices, ensuring that you receive the best value for your money without
        breaking bank.
      </p>
    </div>
  </div>

  <div class="card" use:reveal={{ transition: "slide", delay: 200 }}>
    <figure class="avatar p-5">
      <div
        class="w-60 rounded-full ring ring-primary ring-offset-base-100 ring-offset-4"
      >
        <enhanced:img
          src="../lib/assets/galleryImg6.jpg"
          alt="Quick Turnaround"
          sizes="(max-width: 768px) 100vw, 50vw"
        />
      </div>
    </figure>
    <div class="card-body items-center text-center">
      <h2 class="card-title">Quick Turnaround <Icon icon="ph:clock" /></h2>
      <p>
        I understand how important it is to get your vehicle back on the road
        fast. That is why I strive to deliver fast and timely repair services
        while maintaining high quality standards.
      </p>
    </div>
  </div>

  <div class="md:col-span-3 flex justify-center items-center">
    <ContactBtn />
  </div>
</section>
<div class="pb-20 mb-20">
  <section id="services" class="container mx-auto px-5 py-8">
    <!-- content -->
    <div class="relative bg-base-200 rounded-t-3xl overflow-hidden">
      <!-- image -->
      <div
        class="hero h-80"
        style={`background-image: url(${kiaSorentoFront});`}
      >
        <div class="hero-overlay bg-opacity-60"></div>
        <div class="hero-content text-center text-neutral-content">
          <div use:reveal={{ transition: "blur", delay: 200 }}>
            <h1 class="mb-5 text-5xl font-bold">Fast, Reliable, Cheap</h1>
            <p class="mb-5">
              Experience top-notch auto repair services that won't break the
              bank. With over 10 years of expertise, I have successfully
              repaired 100+ vehicles, offering a full range of services to keep
              your car running smoothly.
            </p>
          </div>
        </div>
      </div>
      <div class="container mx-auto p-5 pt-20 md:pt-24">
        <div
          use:reveal={{ transition: "fade", delay: 200 }}
          class=" md:pt-0 grid grid-cols-1 md:grid-cols-2 gap-4 items-center h-full"
        >
          <div class="space-y-4">
            <h1 class="font-bold">Services</h1>
            <article class="font-semibold">
              <ul class="list-disc list-inside">
                <li>Engine repairs</li>
                <li>Wheel alignments</li>
                <li>Spark plug replacements</li>
                <li>And much more!</li>
              </ul>
            </article>
            <div class="divider" />
            <p>
              Get your vehicle back on the road quickly and affordably. Contact
              me today for all your auto repair needs!
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
              <div class="stat-desc">Dedication to Quality Workmanship</div>
            </div>

            <div class="stat">
              <div class="stat-title font-semibold text-xl">Satisfaction</div>
              <div class="stat-value">98%</div>
              <div class="stat-desc">No Customer Left Unsatisfied</div>
            </div>

            <div class="stat">
              <div class="stat-title font-semibold text-xl">
                Services Offered
              </div>
              <div class="stat-value">15+</div>
              <div class="stat-desc">
                Comprehensive Range of Repair Services
              </div>
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
            src="https://us1-photo.nextdoor.com/user_photos/c9/62/c9620bcfc8dcc4efd38b278656adfb74?request_version=v2&sizing=linear&resize_type=resize&output_type=webp&x_size=1"
            alt="reviewImg"
            class="mask mask-squircle"
          />
        </div>
      </div>
      <blockquote class="flex flex-col justify-center ml-4">
        <cite class="text-lg font-semibold">Maia Bost</cite>
        <p class="text-sm text-neutral-content">
          "Tony really came through for me and my car! He came when he said he
          was gonna come. He was nice, knowledgeable, & respectful. All I had to
          do was buy the part and his price was reasonable!!! Thank you for your
          help Tony."
        </p>
      </blockquote>
    </article>
    <article
      class="border border-accent rounded-lg flex flex-row p-4 shadow-lg"
    >
      <div class="avatar">
        <div class="w-24 rounded-full">
          <img
            src="https://d19rpgkrjeba2z.cloudfront.net/b6c8199a337cd846/static/nextdoorv2/images/avatars/color-5/c.png?request_version=v2&sizing=linear&resize_type=resize&output_type=webp&x_size=1"
            alt="reviewImg"
            class="mask mask-squircle"
          />
        </div>
      </div>
      <blockquote class="flex flex-col justify-center ml-4">
        <cite class="text-lg font-semibold">Christine Davis</cite>
        <p class="text-sm text-neutral-content">
          "his work is top notch. He has been doing repairs on my Honda Civic
          since coming to North Carolina and has never disappointed me."
        </p>
      </blockquote>
    </article>
  </div>
</section>

<section class="bg-base-200 py-16">
  <div class="container mx-auto px-4">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
      <div>
        <h2 class="text-4xl font-bold mb-4">
          Ready to Get Your Car Back on the Road?
        </h2>
        <p class="text-lg mb-6">
          Don't let car troubles keep you from your daily life. With my
          dedication to quality, you'll never have to worry about your car
          again.
        </p>
        <ContactBtn />
      </div>
    </div>
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
