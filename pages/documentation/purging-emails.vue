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
            Purging emails
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
          </p>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <div class="space-y-8">

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">How it works</h3>
            </div>
            <div class="p-6">
	      <p class="text-gray-700 dark:text-gray-300 mb-4">When piler archives a message, it assigns a retention value (=a timestamp) to it. Piler guarantees that the message will sit in the archive at least until its retention time expires.</p>

	      <p class="text-gray-700 dark:text-gray-300 mb-4">The removal of aged emails is done by the pilerpurge.py utility. You must run pilerpurge.py if you want aged emails to be purged, otherwise they will be in the archive for eternity. So if you don’t want emails to be purged, then simply don’t run pilerpurge.py, and comment out the purge job in piler's crontab.</p>

	      <p class="text-gray-700 dark:text-gray-300 mb-4">If you run pilerpurge.py periodically (eg. from crontab), then it first checks whether purging is allowed. If not, then it stops, otherwise it queries the ids of aged messages, then removes them from the disk, and sets their status as deleted in the metadata table.</p>

	      <p class="text-gray-700 dark:text-gray-300 mb-4">Note that to preserve the history of emails, the metadata entries are not deleted.</p>

	      <p class="text-gray-700 dark:text-gray-300 mb-4">In case of an ongoing audit or similar event you may disable the periodic purge. It can be done by administrators on the gui health page.</p>

	      <p class="text-gray-700 dark:text-gray-300 mb-4">Before deploying piler (or any email archiving solution) make sure to have a well established retention policy. If may be as simple as to set the default retention to 7 years or so. It depends on region, industrial sector, legislation environment, etc.</p>

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
  title: 'Installation - Piler Documentation',
  meta: [
    { name: 'description', content: 'Install Piler email archiving system on your server with complete step-by-step instructions.' }
  ]
})
</script>
