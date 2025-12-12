<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  
  // Icons
  const ArrowRight = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>`;
  const PlayCircle = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polygon points="10 8 16 12 10 16 10 8"/></svg>`;
  const ChevronLeft = `<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>`;
  const ChevronRight = `<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>`;
  const Check = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6 9 17l-5-5"/></svg>`;
  const Plus = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="M12 5v14"/></svg>`;
  const Instagram = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></svg>`;
  const LinkedIn = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>`;
  const XIcon = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 6 6 18"/><path d="m6 6 18 12"/></svg>`;

  // Data
  const heroImages = [
    "/generated/image-close-up-of-natural-plant-leaves-with-wa-1765517685282-0.webp",
    "/generated/image-sustainable-skincare-products-with-natur-1765517688117-1.webp",
    "/generated/image-honeycomb-structure-in-nature-with-golde-1765517690627-2.webp",
    "/generated/image-laboratory-scientist-examining-plant-ext-1765517692929-3.webp",
    "/generated/image-organic-botanical-ingredients-arranged-a-1765517695300-4.webp",
    "/generated/image-person-holding-eco-friendly-product-in-n-1765517697784-5.webp"
  ];

  const benefitCards = [
    {
      title: "Nature-backed positioning.",
      desc: "Gain authentic scientific credibility with biomimicry principles that translate nature's 3.8 billion years of R&D into your products.",
      image: "/generated/image-wellness-brand-founder-working-at-desk-w-1765517700033-6.webp"
    },
    {
      title: "Research access you can trust.",
      desc: "Access comprehensive biomimicry research and natural formulation expertise without building your own lab.",
      image: "/generated/image-research-laboratory-with-natural-plant-s-1765517702363-7.webp"
    },
    {
      title: "Sustainable innovation.",
      desc: "Create products that perform better by learning from nature's proven solutions, not synthetic shortcuts.",
      image: "/generated/image-sustainable-product-formulation-with-nat-1765517704612-8.webp"
    }
  ];

  const steps = [
    {
      step: 1,
      title: "Choose your innovation path.",
      desc: "Select from our Starter or Premium biomimicry research packages. Access nature-based formulation principles tailored to your product category.",
      image: "plan"
    },
    {
      step: 2,
      title: "Discovery consultation.",
      desc: "Our biomimicry experts analyze your product goals and identify relevant natural solutions from our research database.",
      image: "schedule"
    },
    {
      step: 3,
      title: "Formulation development.",
      desc: "Receive your custom nature-based formulations with complete ingredient sourcing and scientific documentation.",
      image: "results"
    },
    {
      step: 4,
      title: "Testing and refinement.",
      desc: "We validate formulations for safety and efficacy, providing transparent test results and certification documentation.",
      image: "notes"
    },
    {
      step: 5,
      title: "Launch and scale.",
      desc: "Go to market with confidence. Access ongoing support, marketing materials, and sourcing as you scale to 50K monthly orders.",
      image: "improve"
    }
  ];

  const faqs = [
    "What is biomimicry and how does it apply to product development?",
    "How do you ensure ingredient sustainability and transparency?",
    "What product categories do you work with?",
    "How long does the formulation process take?",
    "Can you help us scale to 50K monthly orders?"
  ];
</script>

<Header />

<main class="w-full overflow-x-hidden">
  <!-- Hero Section -->
  <section class="pt-32 pb-16 md:pt-40 md:pb-24 px-6 text-center max-w-7xl mx-auto">
    <h1 class="text-4xl md:text-6xl lg:text-7xl font-medium tracking-tight text-[#1A1A1A] mb-6 leading-[1.1]">
      Nature's solutions.<br />Your innovation.
    </h1>
    <p class="text-gray-600 text-lg md:text-xl max-w-3xl mx-auto mb-10 leading-relaxed font-light">
      Transform your wellness brand with biomimicry-backed formulations. Access 3.8 billion years of nature's R&D to create products eco-conscious parents trust.
    </p>
    <button class="bg-[#1A1A1A] text-white px-8 py-3.5 rounded-sm font-medium hover:bg-black transition-colors">
      Explore solutions
    </button>
  </section>

  <!-- Hero Images Scroll -->
  <div class="w-full overflow-x-auto pb-12 hide-scrollbar">
    <div class="flex gap-4 px-6 min-w-max">
      {#each heroImages as img, i}
        <div class="relative w-48 h-64 md:w-64 md:h-80 rounded-3xl overflow-hidden flex-shrink-0">
          <img src={img} alt="Nature-inspired sustainable products" class="w-full h-full object-cover" />
        </div>
      {/each}
    </div>
  </div>

  <!-- App Feature Section -->
  <section class="py-20 px-6 max-w-7xl mx-auto">
    <div class="bg-white rounded-[40px] p-8 md:p-16 flex flex-col md:flex-row items-center gap-12 shadow-sm">
      <!-- Phone Mockup -->
      <div class="w-full md:w-1/2 flex justify-center">
        <div class="relative w-[280px] h-[580px] bg-black rounded-[40px] border-[8px] border-black shadow-2xl overflow-hidden">
          <div class="absolute top-0 left-0 right-0 h-6 bg-black z-20 flex justify-center">
            <div class="w-20 h-4 bg-black rounded-b-xl"></div>
          </div>
          <div class="w-full h-full bg-white pt-10 px-4 overflow-hidden flex flex-col">
            <!-- Mock UI -->
            <div class="flex justify-between items-center mb-6">
              <div class="w-8 h-8 rounded-full bg-gray-200"></div>
              <div class="w-8 h-8 rounded-full bg-gray-100"></div>
            </div>
            <div class="mb-6">
              <div class="text-xs text-gray-500 mb-1">30 June</div>
              <div class="text-2xl font-bold">1</div>
            </div>
            <div class="space-y-3">
              <div class="h-20 bg-gray-50 rounded-xl w-full border border-gray-100 p-3">
                <div class="w-1/2 h-2 bg-gray-200 rounded mb-2"></div>
                <div class="w-full h-1 bg-green-400 rounded"></div>
              </div>
              <div class="h-20 bg-gray-50 rounded-xl w-full border border-gray-100 p-3">
                <div class="w-1/2 h-2 bg-gray-200 rounded mb-2"></div>
                <div class="w-full h-1 bg-orange-400 rounded"></div>
              </div>
              <div class="h-20 bg-gray-50 rounded-xl w-full border border-gray-100 p-3">
                <div class="w-1/2 h-2 bg-gray-200 rounded mb-2"></div>
                <div class="w-full h-1 bg-blue-400 rounded"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Content -->
      <div class="w-full md:w-1/2 space-y-8">
        <h2 class="text-3xl md:text-4xl font-medium leading-tight text-[#1A1A1A]">
          Your formulation partner.<br />
          Access our biomimicry research database, track product development, and receive transparent sourcing documentation that builds trust with eco-conscious consumers.
        </h2>
        <div class="flex items-center justify-between pt-4">
          <button class="flex items-center gap-2 text-[#1A1A1A] font-medium hover:opacity-70 transition-opacity">
            {@html PlayCircle}
            Watch demo
          </button>
          <div class="flex gap-2">
            <button class="p-2 rounded-full border border-gray-200 hover:bg-gray-50 text-gray-400 hover:text-black transition-colors">
              {@html ChevronLeft}
            </button>
            <button class="p-2 rounded-full border border-gray-200 hover:bg-gray-50 text-gray-400 hover:text-black transition-colors">
              {@html ChevronRight}
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Value Proposition -->
  <section class="py-16 px-6 max-w-7xl mx-auto">
    <div class="grid md:grid-cols-2 gap-12 items-start">
      <h2 class="text-3xl md:text-5xl font-medium tracking-tight text-[#1A1A1A] leading-tight">
        Nature solved it first. We help you apply it.
      </h2>
      <p class="text-gray-600 text-lg font-light leading-relaxed">
        For 3.8 billion years, nature has been perfecting sustainable solutions. From lotus leaves that self-clean to spider silk stronger than steel, biomimicry unlocks innovation that's both effective and earth-friendly. We translate these principles into commercial products your customers trust.
      </p>
    </div>
  </section>

  <!-- Benefit Cards -->
  <section class="py-8 px-6 max-w-7xl mx-auto">
    <div class="grid md:grid-cols-3 gap-6">
      {#each benefitCards as card}
        <div class="relative h-[480px] rounded-3xl overflow-hidden group">
          <img src={card.image} alt={card.title} class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
          <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-black/20 to-transparent"></div>
          <div class="absolute bottom-0 left-0 right-0 p-8 text-white">
            <h3 class="text-2xl font-medium mb-3">{card.title}</h3>
            <p class="text-white/80 text-sm leading-relaxed font-light">{card.desc}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Testimonial -->
  <section class="py-24 px-6 max-w-4xl mx-auto text-center">
    <blockquote class="text-2xl md:text-3xl font-medium leading-relaxed text-[#1A1A1A] mb-8">
      "Based On Nature gave us the scientific credibility we needed. Parents trust our products now because they can see the transparent research behind every ingredient. Our sales increased 3x in six months."
    </blockquote>
    <div class="flex flex-col items-center gap-3">
      <img src="/generated/image-confident-eco-conscious-mother-with-chil-1765517706851-9.webp" alt="Customer testimonial" class="w-12 h-12 rounded-full object-cover" />
      <div class="text-center">
        <div class="font-medium text-sm">Sarah Chen</div>
        <div class="text-gray-500 text-xs">Founder, Pure Roots Wellness</div>
      </div>
    </div>
  </section>

  <!-- Stats Grid -->
  <section class="py-12 px-6 max-w-7xl mx-auto border-t border-gray-200">
    <div class="grid md:grid-cols-3 gap-8 text-center md:text-left">
      <div>
        <h3 class="text-xl font-medium mb-2">3.8 billion years of R&D.</h3>
        <p class="text-gray-500 text-sm font-light">Nature has already solved your formulation challenges. We help you apply those solutions.</p>
      </div>
      <div>
        <h3 class="text-xl font-medium mb-2">50K monthly orders at scale.</h3>
        <p class="text-gray-500 text-sm font-light">Our partners capture the $150B sustainable products market with proven biomimicry formulations.</p>
      </div>
      <div>
        <h3 class="text-xl font-medium mb-2">Transparent documentation.</h3>
        <p class="text-gray-500 text-sm font-light">Every ingredient sourced and documented to overcome skepticism from eco-conscious parents.</p>
      </div>
    </div>
  </section>

  <!-- How it works -->
  <section class="py-20 px-6 max-w-7xl mx-auto" id="solutions">
    <div class="mb-16 max-w-md">
      <h2 class="text-4xl font-medium mb-6">How it works.</h2>
      <p class="text-gray-600 font-light">From biomimicry research to scalable production, we guide wellness brands through every step of creating nature-backed products that eco-conscious parents trust.</p>
    </div>

    <div class="space-y-6">
      {#each steps as step}
        <div class="bg-white rounded-[40px] p-8 md:p-12 flex flex-col items-center text-center max-w-2xl mx-auto shadow-sm">
          <div class="w-full text-left mb-8">
            <span class="inline-block w-8 h-8 rounded-full border border-gray-200 text-center leading-8 text-sm font-medium mb-4">{step.step}</span>
            <h3 class="text-2xl font-medium mb-3">{step.title}</h3>
            <p class="text-gray-500 font-light text-sm max-w-lg">{step.desc}</p>
          </div>
          
          <!-- Phone Mockup for Step -->
          <div class="relative w-[240px] h-[480px] bg-black rounded-[35px] border-[6px] border-black shadow-xl overflow-hidden mt-4">
             <div class="absolute top-0 left-0 right-0 h-5 bg-black z-20 flex justify-center">
                <div class="w-16 h-3 bg-black rounded-b-lg"></div>
             </div>
             <div class="w-full h-full bg-white pt-8 px-3 overflow-hidden">
                <!-- Dynamic Content based on step -->
                {#if step.image === 'plan'}
                  <div class="space-y-3 mt-4">
                    <div class="p-3 border rounded-xl border-black bg-gray-50">
                      <div class="font-bold text-xs mb-1">Optimal ID</div>
                      <div class="h-1 w-full bg-gray-200 rounded"></div>
                    </div>
                    <div class="p-3 border rounded-xl border-gray-200">
                       <div class="font-bold text-xs mb-1 text-gray-400">Essential</div>
                       <div class="h-1 w-full bg-gray-100 rounded"></div>
                    </div>
                  </div>
                {:else if step.image === 'schedule'}
                   <div class="mt-4">
                     <div class="text-center font-bold mb-4">Appointment</div>
                     <div class="bg-gray-100 h-32 rounded-xl mb-3 flex items-center justify-center text-xs text-gray-400">Map View</div>
                     <button class="w-full bg-black text-white text-xs py-2 rounded-lg">Confirm</button>
                   </div>
                {:else if step.image === 'results'}
                   <div class="bg-black h-full -mx-3 -mt-8 pt-10 px-3 text-white">
                      <div class="text-center mb-6">
                        <div class="w-12 h-12 bg-gray-700 rounded-full mx-auto mb-2"></div>
                        <div class="text-sm font-bold">Grace Parker</div>
                      </div>
                      <div class="space-y-2">
                         <div class="bg-gray-800 p-2 rounded-lg h-10"></div>
                         <div class="bg-gray-800 p-2 rounded-lg h-10"></div>
                      </div>
                   </div>
                {:else if step.image === 'notes'}
                   <div class="mt-4 space-y-3">
                      <div class="font-bold text-sm">Health Status</div>
                      <div class="text-[10px] text-gray-500 leading-relaxed">
                        You usually make smart choices for your health through regular exercise...
                      </div>
                      <div class="bg-gray-50 p-2 rounded text-[10px] text-gray-600">
                        Since your diet lacks enough fruits and vegetables...
                      </div>
                   </div>
                {:else}
                   <div class="mt-4 flex flex-col h-full">
                      <div class="flex-1">
                        <div class="bg-gray-100 p-2 rounded-lg rounded-tl-none text-[10px] mb-2 max-w-[80%]">
                          What benefits can I get by bringing ApoB closer to the optimal range?
                        </div>
                        <div class="bg-blue-50 p-2 rounded-lg rounded-tr-none text-[10px] ml-auto max-w-[80%]">
                          By lowering ApoB, you reduce the number of cholesterol-carrying particles...
                        </div>
                      </div>
                      <div class="h-10 border-t mt-2"></div>
                   </div>
                {/if}
             </div>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Dark Cards Section -->
  <section class="py-8 px-6 max-w-7xl mx-auto">
    <div class="grid md:grid-cols-2 gap-6">
      <!-- Sustainability Card -->
      <div class="bg-[#111] rounded-[40px] p-8 md:p-12 text-white min-h-[500px] flex flex-col relative overflow-hidden">
        <div class="relative z-10">
          <h3 class="text-sm font-medium text-gray-400 mb-2">Certified sustainable.</h3>
          <h2 class="text-2xl md:text-3xl font-medium max-w-xs">Every ingredient traced from source to product.</h2>
        </div>
        <!-- Abstract Nature Pattern Visual -->
        <div class="absolute inset-0 flex items-center justify-center opacity-20 mt-20">
           <svg viewBox="0 0 200 200" class="w-full h-full text-primary-600 fill-current">
              <!-- Leaf/organic pattern -->
              {#each Array(50) as _, i}
                <circle cx={Math.random() * 200} cy={Math.random() * 200} r={Math.random() * 2 + 1} />
              {/each}
           </svg>
        </div>
      </div>

      <!-- Transparency Card -->
      <div class="bg-[#111] rounded-[40px] p-8 md:p-12 text-white min-h-[500px] flex flex-col relative overflow-hidden">
        <div class="relative z-10">
          <h3 class="text-sm font-medium text-gray-400 mb-2">Complete transparency.</h3>
          <h2 class="text-2xl md:text-3xl font-medium max-w-xs">Full documentation builds trust with eco-conscious consumers.</h2>
        </div>
        <!-- Document Visual -->
        <div class="absolute inset-0 flex items-center justify-center mt-20 overflow-hidden">
           <div class="text-sm font-mono text-gray-600 opacity-20 select-none p-8 space-y-2">
             <div>Source: Organic Farm #A2847</div>
             <div>Certification: USDA Organic</div>
             <div>Harvest Date: 2024-01-15</div>
             <div>Processing: Cold-pressed</div>
             <div>Testing: 3rd Party Verified</div>
           </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Pricing Section -->
  <section class="py-24 px-6 max-w-7xl mx-auto" id="join">
    <div class="text-center mb-16">
      <h2 class="text-3xl md:text-4xl font-medium mb-4">Sustainable innovation made accessible.</h2>
      <p class="text-gray-500 font-light max-w-2xl mx-auto">From biomimicry research to scalable formulations, we provide everything wellness brands need to create nature-backed products that eco-conscious consumers trust.</p>
    </div>

    <div class="grid md:grid-cols-2 gap-6 max-w-4xl mx-auto">
      <!-- Starter Plan -->
      <div class="bg-white rounded-[32px] p-8 flex flex-col">
        <div class="w-12 h-12 bg-primary-100 rounded-full mb-6 flex items-center justify-center">
          <div class="w-6 h-6 text-primary-600">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M12 2L2 7l10 5 10-5-10-5z"/>
              <path d="M2 17l10 5 10-5"/>
              <path d="M2 12l10 5 10-5"/>
            </svg>
          </div>
        </div>
        <h3 class="text-2xl font-medium mb-1">Starter</h3>
        <p class="text-sm text-gray-500 mb-6">Begin your biomimicry journey.</p>
        <div class="mb-8">
          <span class="text-2xl font-medium">$2,500</span>
          <span class="text-gray-400 text-sm">/product</span>
          <div class="text-[10px] text-primary-600 mt-1 font-medium">One-time formulation fee</div>
        </div>
        <ul class="space-y-4 mb-8 flex-1">
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Access to biomimicry research database for one product category.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Custom nature-based formulation with ingredient sourcing.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Basic documentation package for marketing transparency.
          </li>
        </ul>
        <button class="w-full bg-[#1A1A1A] text-white py-3 rounded-sm font-medium hover:bg-black transition-colors">Get started</button>
      </div>

      <!-- Premium Plan -->
      <div class="bg-white rounded-[32px] p-8 flex flex-col relative overflow-hidden">
        <div class="absolute top-0 right-0 bg-primary-100 px-4 py-1 rounded-bl-xl text-xs font-medium text-primary-800">Most Popular</div>
        <div class="w-12 h-12 bg-primary-200 rounded-full mb-6 flex items-center justify-center">
          <div class="w-6 h-6 text-primary-700">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="12" cy="12" r="10"/>
              <path d="M12 6v6l4 2"/>
            </svg>
          </div>
        </div>
        <h3 class="text-2xl font-medium mb-1">Premium</h3>
        <p class="text-sm text-gray-500 mb-6">Complete innovation partnership.</p>
        <div class="mb-8">
          <span class="text-2xl font-medium">$5,000</span>
          <span class="text-gray-400 text-sm">/month</span>
          <div class="text-[10px] text-primary-600 mt-1 font-medium">Unlimited product development</div>
        </div>
        <ul class="space-y-4 mb-8 flex-1">
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Full biomimicry research access across all product categories.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Unlimited formulations with testing, validation, and certification support.
          </li>
          <li class="flex items-start gap-3 text-sm text-gray-600 font-light">
            <span class="mt-0.5 text-black">{@html Check}</span>
            Complete transparency documentation, marketing materials, and scaling support to 50K orders/month.
          </li>
        </ul>
        <button class="w-full bg-[#1A1A1A] text-white py-3 rounded-sm font-medium hover:bg-black transition-colors">Get started</button>
      </div>
    </div>
  </section>

  <!-- FAQ -->
  <section class="py-20 px-6 max-w-3xl mx-auto" id="faq">
    <h2 class="text-3xl font-medium text-center mb-12">Your questions answered.</h2>
    <div class="space-y-4">
      {#each faqs as question}
        <div class="border-b border-gray-200 py-4 flex justify-between items-center cursor-pointer group hover:bg-gray-50/50 transition-colors px-2">
          <span class="text-sm md:text-base font-medium text-gray-800">{question}</span>
          <span class="text-gray-400 group-hover:text-black transition-colors">{@html Plus}</span>
        </div>
      {/each}
    </div>
    <div class="mt-12 text-center">
      <button class="border border-gray-300 px-6 py-3 rounded-sm text-xs font-medium hover:bg-gray-50 transition-colors">
        View all Frequently Asked Questions
      </button>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-16 px-6 border-t border-gray-200 bg-[#F9F8F6]">
    <div class="max-w-7xl mx-auto">
      <div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-8 mb-16">
        <div class="flex items-center gap-2">
           <div class="w-6 h-6 text-primary-600">
             <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
               <path
                 opacity="0.5"
                 d="M16.6765 3.05148C18.9425 3.05148 20.7794 4.88843 20.7794 7.15442C20.7794 9.42043 18.9425 11.2574 16.6765 11.2574H12.5735V7.15442C12.5735 4.88843 14.4105 3.05148 16.6765 3.05148Z"
                 fill="currentColor"
               />
               <path
                 d="M3 7.15442C3 4.88843 4.83695 3.05148 7.10294 3.05148C9.36895 3.05148 11.2059 4.88843 11.2059 7.15442V11.2574H7.10294C4.83695 11.2574 3 9.42043 3 7.15442Z"
                 fill="currentColor"
               />
               <path
                 d="M7.10294 20.8309C4.83695 20.8309 3 18.9939 3 16.7279C3 14.4619 4.83695 12.625 7.10294 12.625H11.2059V16.7279C11.2059 18.9939 9.36895 20.8309 7.10294 20.8309Z"
                 fill="currentColor"
               />
               <path
                 d="M20.7794 16.7279C20.7794 18.9939 18.9425 20.8309 16.6765 20.8309C14.4105 20.8309 12.5735 18.9939 12.5735 16.7279V12.625H16.6765C18.9425 12.625 20.7794 14.4619 20.7794 16.7279Z"
                 fill="currentColor"
               />
             </svg>
           </div>
           <span class="font-bold text-lg">Based On Nature</span>
        </div>
        
        <nav class="flex flex-wrap gap-6 md:gap-8 text-xs font-medium text-gray-600">
          <a href="#solutions" class="hover:text-black">Solutions</a>
          <a href="#faq" class="hover:text-black">FAQ</a>
          <a href="#" class="hover:text-black">Research</a>
          <a href="#" class="hover:text-black">Terms & Conditions</a>
          <a href="#" class="hover:text-black">Privacy Policy</a>
        </nav>

        <div class="flex gap-4 text-gray-800">
          <a href="#" class="hover:text-black">{@html XIcon}</a>
          <a href="#" class="hover:text-black">{@html Instagram}</a>
          <a href="#" class="hover:text-black">{@html LinkedIn}</a>
        </div>
      </div>

      <div class="text-[10px] text-gray-400 leading-relaxed max-w-5xl">
        <p class="mb-2">Based On Nature is a biomimicry research and product innovation company. We provide formulation consulting and research services to wellness brands. All product formulations are developed in partnership with certified laboratories and manufacturing facilities. Based On Nature does not manufacture products directly but connects brands with verified sustainable suppliers and production partners.</p>
        <p>Pricing includes research, formulation development, and documentation services. Manufacturing, testing, and certification costs are separate and depend on product specifications and volume. For complete pricing details, see our Terms & Conditions.</p>
        <p class="mt-2">By providing your contact information, you agree to receive communications from Based On Nature about our services. You can unsubscribe at any time.</p>
      </div>
    </div>
  </footer>
</main>

<style>
  :global(body) {
    background-color: #F9F8F6;
    font-family: 'Inter', sans-serif;
  }
  
  .hide-scrollbar::-webkit-scrollbar {
    display: none;
  }
  .hide-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
</style>

