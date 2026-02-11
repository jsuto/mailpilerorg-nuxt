<template>
  <div>
    <!-- Hero Section -->
    <section class="bg-gradient-to-b from-blue-50 to-white dark:from-gray-800 dark:to-gray-900 py-16">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <NuxtLink to="/documentation" class="text-primary-light dark:text-primary-dark hover:underline mb-4 inline-flex items-center text-sm font-medium">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
          </svg>
          Back to Documentation
        </NuxtLink>
        <div class="text-center mt-8">
          <h1 class="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white mb-4">
            Audit
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Search and review the audit trail to track user actions on the archive.
          </p>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <div class="space-y-8">

          <!-- Overview -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Overview</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">
                Piler logs user actions such as searches, logins, email views, and more. The audit feature allows administrators and auditors to search these logs to review what actions users have performed on the archive.
              </p>
              <p class="text-gray-700 dark:text-gray-300">
                The audit page is accessible from the GUI by navigating to <span class="font-mono bg-gray-100 dark:bg-gray-700 px-2 py-0.5 rounded">Administration &rarr; Audit</span>.
              </p>
            </div>
          </div>

          <!-- Search Fields -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Search Fields</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">You can filter the audit log using the following fields:</p>
              <ul class="list-disc list-inside text-gray-700 dark:text-gray-300 space-y-2">
                <li><span class="font-semibold">user</span> &ndash; the email address of the user who performed the action</li>
                <li><span class="font-semibold">action</span> &ndash; the type of action, eg. search, login, view, download, etc.</li>
                <li><span class="font-semibold">date1</span> &ndash; start date for the search range (format: YYYY.MM.DD)</li>
                <li><span class="font-semibold">date2</span> &ndash; end date for the search range (format: YYYY.MM.DD)</li>
                <li><span class="font-semibold">description</span> &ndash; text to search for in the action description</li>
              </ul>
            </div>
          </div>

          <!-- Search Examples -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Search Examples</h3>
            </div>
            <div class="p-6 space-y-6">

              <div>
                <p class="text-gray-700 dark:text-gray-300 mb-2">Find all search actions by a specific user starting from a given date:</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono">user: auditor@local<br>action: search<br>date1: 2026.01.11</code>
                </div>
              </div>

              <div>
                <p class="text-gray-700 dark:text-gray-300 mb-2">Find all login actions in a date range:</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono">action: login<br>date1: 2026.01.01<br>date2: 2026.01.31</code>
                </div>
              </div>

              <div>
                <p class="text-gray-700 dark:text-gray-300 mb-2">Find all actions performed by a specific user:</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono">user: admin@local</code>
                </div>
              </div>

            </div>
          </div>

        </div>

        <!-- Additional Resources -->
        <div class="mt-16 bg-gradient-to-br from-blue-50 to-indigo-50 dark:from-gray-800 dark:to-gray-700 rounded-xl shadow-lg border border-gray-200 dark:border-gray-600 p-8">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-6 text-center">
            Additional Resources
          </h3>
          <div class="grid md:grid-cols-1 gap-4">
            <a href="https://github.com/jsuto/piler/issues" target="_blank" rel="noopener noreferrer" class="block bg-white dark:bg-gray-800 rounded-lg p-6 hover:shadow-md transition-shadow border border-gray-200 dark:border-gray-700">
              <div class="flex items-center mb-3">
                <svg class="h-6 w-6 text-primary-light dark:text-primary-dark mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
                </svg>
                <span class="font-semibold text-gray-900 dark:text-white">Get Help</span>
              </div>
              <p class="text-sm text-gray-600 dark:text-gray-400">Community support</p>
            </a>
          </div>
        </div>

      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Audit - Piler Documentation',
  meta: [
    { name: 'description', content: 'Search and review the audit trail to track user actions on the Piler email archive.' }
  ]
})
</script>
