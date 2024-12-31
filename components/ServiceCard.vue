<script setup>
defineProps({
  icon: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  buttonText: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="border-2 border-white/20 rounded-xl p-8 backdrop-blur-sm hover:border-white/40 transition-colors duration-200 flex flex-col h-full">
    <div class="flex-grow">
      <div class="w-12 h-12 mb-6">
        <Icon :name="icon" class="w-full h-full" />
      </div>
      <h3 class="text-2xl font-bold mb-4">{{ title }}</h3>
      <p class="text-lg text-gray-300">
        {{ description }}
      </p>
    </div>
    <button
      class="w-full bg-transparent border-2 border-white/20 hover:border-white/40 py-2 rounded-lg transition-colors duration-200 mt-8">
      {{ buttonText }}
    </button>
  </div>
</template> 