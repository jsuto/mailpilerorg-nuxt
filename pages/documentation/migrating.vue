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
            Migrating to a New Node
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Migrate your Piler installation to a new server with minimal downtime and complete data integrity.
          </p>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <!-- Overview Section -->
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 dark:from-gray-800 dark:to-gray-700 rounded-xl shadow-lg border border-gray-200 dark:border-gray-600 p-8 mb-8">
          <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-4">
            Migration Overview
          </h2>
          <p class="text-gray-700 dark:text-gray-300 mb-4">
            There are two primary methods for migrating your Piler installation to a new server. Choose the method that best suits your needs:
          </p>
          <div class="grid md:grid-cols-2 gap-6 mt-6">
            <div class="bg-white dark:bg-gray-800 rounded-lg p-6 border-2 border-blue-200 dark:border-blue-700">
              <h3 class="text-lg font-bold text-gray-900 dark:text-white mb-3">Method 1: Export/Import</h3>
              <p class="text-sm text-gray-600 dark:text-gray-400 mb-3">
                Use Piler's built-in export and import functionality to transfer data.
              </p>
              <div class="space-y-2 text-sm">
                <div class="flex items-start">
                  <svg class="h-5 w-5 text-green-500 mr-2 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Cleaner, more controlled process</span>
                </div>
                <div class="flex items-start">
                  <svg class="h-5 w-5 text-green-500 mr-2 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Works across different versions</span>
                </div>
                <div class="flex items-start">
                  <svg class="h-5 w-5 text-yellow-500 mr-2 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">May take longer for large datasets</span>
                </div>
              </div>
            </div>
            <div class="bg-white dark:bg-gray-800 rounded-lg p-6 border-2 border-purple-200 dark:border-purple-700">
              <h3 class="text-lg font-bold text-gray-900 dark:text-white mb-3">Method 2: Raw Data Copy</h3>
              <p class="text-sm text-gray-600 dark:text-gray-400 mb-3">
                Directly copy MySQL, Manticore, and file system data.
              </p>
              <div class="space-y-2 text-sm">
                <div class="flex items-start">
                  <svg class="h-5 w-5 text-green-500 mr-2 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Faster for large installations</span>
                </div>
                <div class="flex items-start">
                  <svg class="h-5 w-5 text-green-500 mr-2 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Complete system state transfer</span>
                </div>
                <div class="flex items-start">
                  <svg class="h-5 w-5 text-yellow-500 mr-2 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Requires identical software versions</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="space-y-8">

          <!-- Method 1: Export/Import -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border-l-4 border-blue-500 dark:border-blue-600 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h2 class="text-2xl font-bold text-white">Method 1: Export/Import</h2>
            </div>
            <div class="p-6 space-y-6">

              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 1: Install Piler on NEW Node</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  See fresh <NuxtLink to="/documentation/installation" class="text-primary-light dark:text-primary-dark hover:underline mb-4 inline-flex items-center text-sm font-medium">installation steps</NuxtLink> on the new server. 
                </p>
              </div>
              
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 2: Update your mail server's config to send emails to NEW Node</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                </p>
              </div>

              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 3: Verify the switch</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Verify that emails are now being archived on NEW node
                </p>
              </div>

              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 4: Export Data on OLD Node</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">Export all emails to current directory</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                  <code class="text-green-400 text-sm font-mono">pilerexport -A</code>
                </div>

                <p class="text-gray-700 dark:text-gray-300 mb-4">OR export all emails, one day at a time to a zip file, eg.</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                  <code class="text-green-400 text-sm font-mono">
                    <p>pilerexport --zip 20251219.zip --start-date 2025.12.19 --stop-date 2025.12.19</p>
                    <p>pilerexport --zip 20251220.zip --start-date 2025.12.20 --stop-date 2025.12.20</p>
                    <p>pilerexport --zip .....zip --start-date ..... --stop-date ....</p>
                  </code>
                </div>
		<p class="text-gray-700 dark:text-gray-300 mb-4">Be sure to script it to cover all dates.</p>
		<p class="text-gray-700 dark:text-gray-300 mb-4">Hint: use a tmux session or similar, because this takes quite some time.</p>

              </div>

              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 5: Copy data to NEW Node</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
		  You may use a network share in the first place where you export the data to.
                </p>
              </div>

              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 6: Import Data on NEW Node</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Assuming data is in /mnt/emldir directory, run the below command
                </p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                  <code class="text-green-400 text-sm font-mono">pilerimport -r -d /mnt/emldir</code>
                </div>

		<p class="text-gray-700 dark:text-gray-300 mb-4">The above command imports all eml files, and removes what's already processed</p>
              </div>

              <!-- Step 4: Verify -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 7: Verify Migration</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Verify that legacy emails are gradually present on NEW node
                </p>
              </div>
            </div>
          </div>

          <!-- Method 2: Raw Data Copy -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border-l-4 border-purple-500 dark:border-purple-600 overflow-hidden">
            <div class="bg-gradient-to-r from-purple-500 to-purple-600 dark:from-purple-600 dark:to-purple-700 px-6 py-4">
              <h2 class="text-2xl font-bold text-white">Method 2: Raw Data Copy</h2>
            </div>
            <div class="p-6 space-y-6">

              <!-- Important Warning -->
              <div class="bg-yellow-50 dark:bg-yellow-900/20 border-l-4 border-yellow-400 p-4">
                <div class="flex">
                  <div class="flex-shrink-0">
                    <svg class="h-5 w-5 text-yellow-400" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M8.257 3.099c.765-1.36 2.722-1.36 3.486 0l5.58 9.92c.75 1.334-.213 2.98-1.742 2.98H4.42c-1.53 0-2.493-1.646-1.743-2.98l5.58-9.92zM11 13a1 1 0 11-2 0 1 1 0 012 0zm-1-8a1 1 0 00-1 1v3a1 1 0 002 0V6a1 1 0 00-1-1z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <div class="ml-3">
                    <p class="text-sm text-yellow-700 dark:text-yellow-300">
                      <strong>Important:</strong> This method requires identical Piler, MySQL, and Manticore versions on both OLD and NEW nodes. Stop all Piler services before proceeding.
                    </p>
                  </div>
                </div>
              </div>

              <!-- Step 1: Prepare OLD node -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 1: Stop Services on OLD Node</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Stop Piler, MySQL, and Manticore services
                </p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono"># </code>
                </div>
              </div>

              <!-- Step 2: Copy MySQL data -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 2: Copy MySQL Database</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Copy raw MySQL data directory or using mysqldump
                </p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono"># </code>
                </div>
              </div>

              <!-- Step 3: Copy Manticore data -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 3: Copy Manticore Indexes</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Copy Manticore index files
                </p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono"># </code>
                </div>
              </div>

              <!-- Step 4: Copy email store -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 4: Copy Email Archive Files</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Copy the email archive directory (typically /var/piler/store)
                </p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono"># Use rsync or scp commands </code>
                </div>
              </div>

              <!-- Step 5: Copy configuration -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 5: Copy Configuration Files</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Copy piler.conf, piler.key, and other configuration files
                </p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono"># </code>
                </div>
              </div>

              <!-- Step 6: Start services -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 6: Start Services on NEW Node</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
                  Start and verify services on the new node
                </p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono"># </code>
                </div>
              </div>

              <!-- Step 7: Verify -->
              <div>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Step 7: Verify Migration</h3>
                <p class="text-gray-700 dark:text-gray-300 mb-4">
		  Verify that all daemons are running, and the UI displays the archived emails just fine.
                </p>
              </div>
            </div>
          </div>

        </div>

        <!-- Additional Resources -->
        <div class="mt-16 bg-gradient-to-br from-blue-50 to-indigo-50 dark:from-gray-800 dark:to-gray-700 rounded-xl shadow-lg border border-gray-200 dark:border-gray-600 p-8">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-6 text-center">
            Additional Resources
          </h3>
          <div class="grid md:grid-cols-2 gap-4">
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
  title: 'Migrating to a New Node - Piler Documentation',
  meta: [
    { name: 'description', content: 'Migrate your Piler installation to a new server with minimal downtime and complete data integrity.' }
  ]
})
</script>
