<script>
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 px-6 py-5 flex items-center justify-between {isScrolled ? 'bg-[#F9F8F6]/90 backdrop-blur-md shadow-sm' : 'bg-transparent'}">
  <div class="flex items-center">
    <!-- Logo -->
    <a href="/" class="flex items-center gap-2 group">
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
      <span class="font-bold text-lg text-[#1A1A1A]">Based On Nature</span>
    </a>
  </div>

  <div class="flex items-center gap-8">
    <nav class="hidden md:flex items-center gap-8 text-[13px] font-medium text-gray-600">
      <a href="#solutions" class="hover:text-black transition-colors">Solutions</a>
      <a href="#faq" class="hover:text-black transition-colors">FAQ</a>
    </nav>
    <a href="#join" class="bg-[#1A1A1A] text-white text-[13px] font-medium px-5 py-2.5 rounded-sm hover:bg-black transition-colors">
      Get started
    </a>
  </div>
</header>