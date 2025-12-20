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
            Importing Emails
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Import existing emails into Piler from various sources including EML or MBOX files, IMAP, and POP3 accounts.
          </p>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <!-- Placeholder Sections -->
        <div class="space-y-8">

          <!-- Import from EML -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Import local emails</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Import from a directory containing EML files</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>pilerimport -d /path/to/dir</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4">Import emails from an MBOX file</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>pilerimport -m /path/to/mbox</p>
                </code>
              </div>

            </div>
          </div>

          <!-- Import from IMAP/POP3 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Import from IMAP/POP3</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Import from IMAP server for user joe, except the Draft folder</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>pilerimport -i imaps://imap.example.com -u joe -p secretpassword -x draft</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4">Import from POP3 server for user joe, except the Draft folder</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>pilerimport -K pop3.example.com -u joe -p secretpassword</p>
                </code>
              </div>
            </div>
          </div>

          <!-- PST -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Import PST files</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Piler can't process PST files directly, you need to extract the individual emails from it. The recommended solution is to use an external utility on Windows.</p>
            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Exchange impersonation</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Replace ‘username’ with your email user (no @domain necessary), ‘superuser’ with your import user, and ‘superpassword’ with your import user’s password, and ‘example.com’ with your domain.</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
		  <p>add-mailboxpermission username -AccessRights FullAccess -user superuser</p>
		  <p>pilerimport -i imaps://imap.example.com -u example.com/superuser/username -p superpassword</p>
		  <p>remove-mailboxpermission username -AccessRights FullAccess -user superuser</p>
                </code>
              </div>

            </div>
          </div>

	  <!-- Notes -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Notes</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">The pilerimport utility runs as user piler (setuid/setgid to piler), therefore the current directory must be writable by the piler user, also the files and directories to Import from must be readable for piler user.</p>
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
  title: 'Importing Emails - Piler Documentation',
  meta: [
    { name: 'description', content: 'Import existing emails into Piler from PST, EML, IMAP, and POP3 sources.' }
  ]
})
</script>
