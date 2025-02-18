<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  document.body.classList.add('page-loaded')
})

useHead({
  title: 'Speed Code Academy | Simple and Effective Software Training',
  meta: [
    {
      name: 'description',
      content: 'Speed Code Academy is a company that aims to help people learn to build quality software as FAST as possible.'
    }
  ]
})
</script>

<template>
  <div class="min-h-screen text-white bg-navy">
    <!-- Header -->
    <header class="animate-fade-in">
      <!-- Navbar -->
      <div class="container mx-auto px-4 flex items-center justify-between">
        <!-- Logo -->
        <NuxtLink class="inline-block h-28 aspect-square" to="/">
          <img src="/logos/logo-edited-solid-background-cropped.png" alt="Logo" class="w-full h-full" />
        </NuxtLink>

        <!-- Navigation Links and Social Icons -->
        <div class="flex items-center gap-8">
          <nav class="flex gap-8 items-center">
            <a 
              href="#services" 
              class="text-lg text-white/80 hover:text-white transition-colors duration-200"
            >
              Services
            </a>
            <a 
              href="#about" 
              class="text-lg text-white/80 hover:text-white transition-colors duration-200"
            >
              About
            </a>
          </nav>
          
          <!-- Social Icons -->
          <div class="flex gap-4 border-l border-white/10 pl-8">
            <a 
              href="https://www.instagram.com/speedcodeacademy/" 
              target="_blank"
              rel="noopener noreferrer"
              class="text-white/80 hover:text-white transition-colors duration-200"
              title="Follow us on Instagram"
            >
              <Icon name="mdi:instagram" class="w-6 h-6" />
            </a>
            <a 
              href="https://www.youtube.com/@speedcodeacademyofficial" 
              target="_blank"
              rel="noopener noreferrer"
              class="text-white/80 hover:text-white transition-colors duration-200"
              title="Subscribe to our YouTube channel"
            >
              <Icon name="mdi:youtube" class="w-6 h-6" />
            </a>
          </div>
        </div>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="min-h-[calc(100vh-7rem)] flex items-center relative">
      <ClientOnly>
        <NuxtParticles
          class="absolute inset-0 -z-10"
          :options="{
            particles: {
              color: {
                value: '#ffffff'
              },
              opacity: {
                value: 0.3
              },
              number: {
                value: 100,
                density: {
                  enable: true,
                  value_area: 800
                }
              },
              size: {
                value: 2
              },
              move: {
                enable: true,
                speed: 0.8,
                direction: 'none',
                random: true,
                straight: false,
                out_mode: 'out',
                bounce: false,
              },
              links: {
                enable: true,
                distance: 150,
                color: '#ffffff',
                opacity: 0.1,
                width: 1
              },
              interactivity: {
                detect_on: 'canvas',
                events: {
                  onhover: {
                    enable: true,
                    mode: 'repulse'
                  },
                  onclick: {
                    enable: true,
                    mode: 'push'
                  },
                  resize: true
                },
                modes: {
                  repulse: {
                    distance: 100,
                    duration: 0.4
                  },
                  push: {
                    particles_nb: 4
                  }
                }
              }
            }
          }"
        />
      </ClientOnly>
      <div class="container mx-auto px-10">
        <hgroup class="animate-slide-up">
          <h1 class="text-6xl font-bold max-w-4xl leading-tight">
            Simple and Effective Software Training
          </h1>
          <p class="text-3xl font-normal block mt-4 animate-fade-in opacity-0" style="animation-delay: 400ms">
            To help people learn to build quality software as FAST as possible.
          </p>
        </hgroup>
        <div class="mt-8 animate-fade-in opacity-0" style="animation-delay: 800ms">
          <button class="bg-gradient-to-t from-gradient-orange-dark to-[#e8dd69] px-8 py-3 rounded-lg font-semibold hover:opacity-90 transition-opacity duration-200">
            Get Started
          </button>
        </div>
        <!-- Scroll Indicator -->
        <div class="absolute bottom-8 left-1/2 -translate-x-1/2 opacity-0 animate-fade-in" style="animation-delay: 1200ms">
          <div class="animate-bounce">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
            </svg>
          </div>
        </div>
      </div>
    </section>
    <!-- Services Section -->
    <section id="services" class="py-16 scroll-mt-28 reveal-on-scroll">
      <h2 class="text-6xl font-bold text-center">
        What we offer
      </h2>
      <div class="container mx-auto px-10 mt-12 grid grid-cols-1 md:grid-cols-3 gap-8">
        <ServiceCard 
          icon="ph:users-bold"
          title="1-on-1 Code Mentorship"
          description="Get personalized guidance and accelerate your learning with direct access to experienced developers who can help you overcome challenges."
          buttonText="Learn More"
        />
        
        <ServiceCard 
          icon="ph:code-bold"
          title="DFY Software Builds"
          description="Let us handle your software development needs with our Done-For-You service. Quality code, delivered on time, built to your specifications."
          buttonText="Get Started"
        />
        
        <ServiceCard 
          icon="ph:graduation-cap-bold"
          title="Courses (Coming Soon)"
          description="Structured learning paths and comprehensive courses designed to take you from beginner to professional. Stay tuned for our upcoming releases."
          buttonText="Join Waitlist"
        />
      </div>
    </section>
    <!-- About Us Section -->
    <section id="about" class="py-16 bg-white/5 scroll-mt-28 reveal-on-scroll">
      <div class="container mx-auto px-10">
        <h2 class="text-6xl font-bold text-center mb-12">
          About Us
        </h2>
        <div class="max-w-6xl mx-auto">
          <div class="flex flex-col md:flex-row items-center gap-12 lg:gap-16">
            <div class="w-64 h-64 flex-shrink-0">
              <img 
                src="/zack-square-image.jpg" 
                alt="Zack Plauché" 
                class="w-full h-full object-cover rounded-full border-4 border-white/10"
              />
            </div>
            <div class="space-y-6 text-lg text-white/80 md:max-w-xl lg:max-w-2xl">
              <p>
                Hi, I'm Zack Plauché, founder of Speed Code Academy. I created this platform because I was frustrated with the 
                state of software education – too many tutorials filled with unnecessary fluff that didn't actually improve my coding skills.
              </p>
              <p>
                Our mission is simple: help people spend less time watching tutorials and more time actually building software. 
                I believe the fastest way to become a better developer is through hands-on experience, not endless video courses.
              </p>
              <p>
                At Speed Code Academy, we cut through the noise and focus on what matters – practical, efficient learning that 
                gets you building real software as quickly as possible. Because the truth is, you learn better and faster when 
                you're actively creating, not passively consuming content.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Footer -->
    <footer class="py-8 border-t border-white/10">
      <div class="container mx-auto px-4 text-center">
        <div class="flex justify-center gap-6 mb-4">
          <a 
            href="https://www.instagram.com/speedcodeacademy/" 
            target="_blank"
            rel="noopener noreferrer"
            class="text-white/60 hover:text-white transition-colors duration-200"
            title="Follow us on Instagram"
          >
            <Icon name="mdi:instagram" class="w-6 h-6" />
          </a>
          <a 
            href="https://www.youtube.com/@speedcodeacademyofficial" 
            target="_blank"
            rel="noopener noreferrer"
            class="text-white/60 hover:text-white transition-colors duration-200"
            title="Subscribe to our YouTube channel"
          >
            <Icon name="mdi:youtube" class="w-6 h-6" />
          </a>
        </div>
        <p class="text-white/60">&copy; {{ new Date().getFullYear() }} Speed Code Academy. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<style>
/* Base animations */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Animation classes */
.animate-fade-in {
  animation: fadeIn 0.6s ease-out forwards;
}

.animate-slide-up {
  animation: slideUp 0.6s ease-out forwards;
}

/* Reveal on scroll */
.reveal-on-scroll {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.reveal-on-scroll.revealed {
  opacity: 1;
  transform: translateY(0);
}

/* Initial state */
.page-loaded .opacity-0 {
  opacity: 0;
}
</style>

<script>
// Add this to handle reveal on scroll
if (import.meta.client) {
  const observerOptions = {
    threshold: 0.1
  }

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('revealed')
      }
    })
  }, observerOptions)

  // Observe all elements with reveal-on-scroll class
  setTimeout(() => {
    document.querySelectorAll('.reveal-on-scroll').forEach((el) => {
      observer.observe(el)
    })
  }, 100)
}
</script>