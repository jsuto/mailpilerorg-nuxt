<template>
  <a
    v-if="isExternal"
    :href="link"
    target="_blank"
    rel="noopener noreferrer"
    class="block bg-white dark:bg-gray-800 p-6 rounded-lg shadow-md border border-gray-200 dark:border-gray-700 hover:shadow-lg hover:border-primary-light dark:hover:border-primary-dark transition-all group"
  >
    <div class="flex items-start">
      <div class="flex-shrink-0 mr-4">
        <div class="w-12 h-12 rounded-lg bg-blue-100 dark:bg-blue-900 flex items-center justify-center group-hover:bg-primary-light dark:group-hover:bg-primary-dark transition-colors">
          <!-- Download Icon -->
          <svg v-if="icon === 'download'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
          </svg>
          <!-- Upload Icon -->
          <svg v-else-if="icon === 'upload'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L9 8m4-4v12" />
          </svg>
          <!-- Speedometer Icon -->
          <svg v-else-if="icon === 'speedometer'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
          </svg>
          <!-- Import Icon -->
          <svg v-else-if="icon === 'import'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12" />
          </svg>
          <!-- Export Icon -->
          <svg v-else-if="icon === 'export'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M9 19l3 3m0 0l3-3m-3 3V10" />
          </svg>
          <!-- Migrate Icon -->
          <svg v-else-if="icon === 'migrate'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4" />
          </svg>
          <!-- User Icon -->
          <svg v-else-if="icon === 'user'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
          </svg>
          <!-- Authentication Icon -->
          <svg v-else-if="icon === 'authentication'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 7a2 2 0 012 2m4 0a6 6 0 01-7.743 5.743L11 17H9v2H7v2H4a1 1 0 01-1-1v-2.586a1 1 0 01.293-.707l5.964-5.964A6 6 0 1121 9z" />
          </svg>
          <!-- Remove Icon -->
          <svg v-else-if="icon === 'remove'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
          </svg>
          <!-- Purge Icon -->
          <svg v-else-if="icon === 'purge'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2M3 12l6.414 6.414a2 2 0 001.414.586H19a2 2 0 002-2V7a2 2 0 00-2-2h-8.172a2 2 0 00-1.414.586L3 12z" />
          </svg>
          <!-- External Link Icon -->
          <svg v-else-if="icon === 'external'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
          </svg>
          <!-- Default Document Icon -->
          <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
          </svg>
        </div>
      </div>
      <div class="flex-1">
        <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2 group-hover:text-primary-light dark:group-hover:text-primary-dark transition-colors">
          {{ title }}
        </h3>
        <p class="text-gray-600 dark:text-gray-400 text-sm">
          {{ description }}
        </p>
      </div>
      <div class="flex-shrink-0 ml-2">
        <!-- External Link Arrow Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400 group-hover:text-primary-light dark:group-hover:text-primary-dark transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
        </svg>
      </div>
    </div>
  </a>
  <NuxtLink
    v-else
    :to="link"
    class="block bg-white dark:bg-gray-800 p-6 rounded-lg shadow-md border border-gray-200 dark:border-gray-700 hover:shadow-lg hover:border-primary-light dark:hover:border-primary-dark transition-all group"
  >
    <div class="flex items-start">
      <div class="flex-shrink-0 mr-4">
        <div class="w-12 h-12 rounded-lg bg-blue-100 dark:bg-blue-900 flex items-center justify-center group-hover:bg-primary-light dark:group-hover:bg-primary-dark transition-colors">
          <!-- Download Icon -->
          <svg v-if="icon === 'download'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
          </svg>
          <!-- Upload Icon -->
          <svg v-else-if="icon === 'upload'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L9 8m4-4v12" />
          </svg>
          <!-- Speedometer Icon -->
          <svg v-else-if="icon === 'speedometer'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
          </svg>
          <!-- Import Icon -->
          <svg v-else-if="icon === 'import'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12" />
          </svg>
          <!-- Export Icon -->
          <svg v-else-if="icon === 'export'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M9 19l3 3m0 0l3-3m-3 3V10" />
          </svg>
          <!-- Migrate Icon -->
          <svg v-else-if="icon === 'migrate'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4" />
          </svg>
          <!-- User Icon -->
          <svg v-else-if="icon === 'user'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
          </svg>
          <!-- Authentication Icon -->
          <svg v-else-if="icon === 'authentication'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 7a2 2 0 012 2m4 0a6 6 0 01-7.743 5.743L11 17H9v2H7v2H4a1 1 0 01-1-1v-2.586a1 1 0 01.293-.707l5.964-5.964A6 6 0 1121 9z" />
          </svg>
          <!-- Remove Icon -->
          <svg v-else-if="icon === 'remove'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
          </svg>
          <!-- Purge Icon -->
          <svg v-else-if="icon === 'purge'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2M3 12l6.414 6.414a2 2 0 001.414.586H19a2 2 0 002-2V7a2 2 0 00-2-2h-8.172a2 2 0 00-1.414.586L3 12z" />
          </svg>
          <!-- External Link Icon -->
          <svg v-else-if="icon === 'external'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
          </svg>
          <!-- Default Document Icon -->
          <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-primary-light dark:text-primary-dark group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
          </svg>
        </div>
      </div>
      <div class="flex-1">
        <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2 group-hover:text-primary-light dark:group-hover:text-primary-dark transition-colors">
          {{ title }}
        </h3>
        <p class="text-gray-600 dark:text-gray-400 text-sm">
          {{ description }}
        </p>
      </div>
      <div class="flex-shrink-0 ml-2">
        <!-- Internal Link Arrow Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400 group-hover:text-primary-light dark:group-hover:text-primary-dark transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
        </svg>
      </div>
    </div>
  </NuxtLink>
</template>

<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  title: string
  description: string
  link: string
  icon?: string
}>()

const isExternal = computed(() => {
  return props.link.startsWith('http://') || props.link.startsWith('https://')
})
</script>
