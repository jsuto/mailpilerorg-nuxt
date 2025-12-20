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
            Configuring the mail server
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            You need to configure your mail server to pass a copy of each received email (both incoming and outgoing) to piler via SMTP protocol.
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
              <h3 class="text-xl font-bold text-white">Postfix</h3>
            </div>
            <div class="p-6">

              <p class="text-gray-700 dark:text-gray-300 mb-4">/etc/postfix/main.cf:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
		  <p>smtpd_recipient_restrictions = reject_non_fqdn_recipient, ..., \</p>
                  <p>&nbsp;&nbsp;&nbsp;check_recipient_access pcre:$config_directory/x-add-envelope-to, ... </p>
		  <p>always_bcc = archive@archive.example.com</p>
		</code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4">/etc/postfix/x-add-envelope-to</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>/(.*)/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;prepend X-Envelope-To: $1</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4">Note that such configuration might reveal Bcc addresses to the recipients in the To/Cc fields. To prevent it happening piler features the HEADER_LINE_TO_HIDE config.php variable to automatically hide the X-Envelope-To: line.</p>
              <p class="text-gray-700 dark:text-gray-300 mb-4">When set (and the default is as seen below) it will hide such header lines from regular users on the GUI, only auditors are allowed to see all recipients, including the Bcc addresses.</p>

              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>$config['HEADER_LINE_TO_HIDE'] = 'X-Envelope-To:';</p>
                </code>
              </div>

            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Exim</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Add the following at the beginning of the routers-section:</p>
	      <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
		  <p>begin routers</p>
                  <p>&nbsp;&nbsp;</p>
                  <p>mailarchive:</p>
                  <p>&nbsp;&nbsp;debug_print = "R: mailarchive for $local_part@$domain"</p>
                  <p>&nbsp;&nbsp;driver = manualroute</p>
                  <p>&nbsp;&nbsp;domains = *</p>
                  <p>&nbsp;&nbsp;transport = remote_smtp</p>
                  <p>&nbsp;&nbsp;# piler listening on port 25:</p>
                  <p>&nbsp;&nbsp;route_list = * "archive.example.com::25"</p>
                  <p>&nbsp;&nbsp;self = send</p>
                  <p>&nbsp;&nbsp;</p>
                  <p>&nbsp;&nbsp;unseen</p>
		</code>
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
  title: 'Installation - Piler Documentation',
  meta: [
    { name: 'description', content: 'Install Piler email archiving system on your server with complete step-by-step instructions.' }
  ]
})
</script>
