<template>
  <div class="min-h-screen flex flex-col">
    <Navbar />
    <main class="flex-grow">
      <slot />
    </main>
    <footer class="bg-gray-100 dark:bg-gray-800 border-t border-gray-200 dark:border-gray-700 py-8 mt-auto">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center text-gray-600 dark:text-gray-400">
          <p>&copy; {{ new Date().getFullYear() }} Piler. Open Source Email Archiving Solution.</p>
        </div>
      </div>
    </footer>
  </div>
</template>
