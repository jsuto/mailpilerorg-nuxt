<template>
  <div>
    <!-- Hero Section -->
    <section class="bg-gradient-to-b from-blue-50 to-white dark:from-gray-800 dark:to-gray-900 py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <h1 class="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white mb-4">
            Documentation
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Everything you need to install, configure, and maintain your Piler email archiving system.
          </p>
        </div>
      </div>
    </section>

    <!-- Documentation Topics -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <!-- Getting Started -->
        <div class="mb-12">
          <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-6 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-light dark:text-primary-dark mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
            Getting Started
          </h2>
          <div class="grid md:grid-cols-2 gap-4">
            <DocCard
              title="Installation"
              description="Step-by-step guide to install Piler on your server, including system requirements and dependencies."
              link="/documentation/installation"
              icon="download"
            />
            <DocCard
              title="Upgrade"
              description="Instructions for upgrading Piler to the latest version while preserving your data and configuration."
              link="/documentation/upgrade"
              icon="upload"
            />
          </div>
        </div>

        <!-- Configuration & Optimization -->
        <div class="mb-12">
          <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-6 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-light dark:text-primary-dark mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6V4m0 2a2 2 0 100 4m0-4a2 2 0 110 4m-6 8a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4m6 6v10m6-2a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4" />
            </svg>
            Configuration & Optimization
          </h2>
          <div class="grid md:grid-cols-2 gap-4">
            <DocCard
              title="Performance Tuning"
              description="Optimize Piler for your workload with tips on database tuning, indexing, and resource allocation."
              link="/documentation/performance-tuning"
              icon="speedometer"
            />
          </div>
        </div>

        <!-- Data Management -->
        <div class="mb-12">
          <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-6 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-light dark:text-primary-dark mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4" />
            </svg>
            Data Management
          </h2>
          <div class="grid md:grid-cols-2 gap-4">
            <DocCard
              title="Importing Emails"
              description="Import existing emails from various sources including PST files, EML files, IMAP, and POP3 accounts."
              link="/documentation/importing-emails"
              icon="import"
            />
            <DocCard
              title="Exporting Emails"
              description="Export archived emails to EML format or restore them to mailboxes for compliance and recovery."
              link="/documentation/exporting-emails"
              icon="export"
            />
            <DocCard
              title="Migrating to a New Node"
              description="Migrate your Piler installation to a new server with minimal downtime and data integrity."
              link="/documentation/migrating"
              icon="migrate"
            />
          </div>
        </div>

        <!-- Quick Links -->
        <div class="bg-gradient-to-r from-blue-50 to-indigo-50 dark:from-gray-800 dark:to-gray-700 rounded-lg p-8 border border-gray-200 dark:border-gray-600">
          <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-6">
            Additional Resources
          </h2>
          <div class="grid md:grid-cols-2 gap-6">
            <div>
              <h3 class="font-semibold text-gray-900 dark:text-white mb-3 flex items-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
                </svg>
                Community Support
              </h3>
              <p class="text-gray-700 dark:text-gray-300 mb-3">
                Get help from the Piler community, report issues, and contribute to the project.
              </p>
              <a
                href="https://github.com/jsuto/piler/issues"
                target="_blank"
                rel="noopener noreferrer"
                class="text-primary-light dark:text-primary-dark hover:underline inline-flex items-center"
              >
                GitHub Issues
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                </svg>
              </a>
            </div>
            <div>
              <h3 class="font-semibold text-gray-900 dark:text-white mb-3 flex items-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
                </svg>
                Source Code
              </h3>
              <p class="text-gray-700 dark:text-gray-300 mb-3">
                Browse the source code, fork the project, and contribute to Piler development.
              </p>
              <a
                href="https://github.com/jsuto/piler/"
                target="_blank"
                rel="noopener noreferrer"
                class="text-primary-light dark:text-primary-dark hover:underline inline-flex items-center"
              >
                View on GitHub
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                </svg>
              </a>
            </div>
            <div>
              <h3 class="font-semibold text-gray-900 dark:text-white mb-3 flex items-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 15l-2 5L9 9l11 4-5 2zm0 0l5 5M7.188 2.239l.777 2.897M5.136 7.965l-2.898-.777M13.95 4.05l-2.122 2.122m-5.657 5.656l-2.12 2.122" />
                </svg>
                Try the Demo
              </h3>
              <p class="text-gray-700 dark:text-gray-300 mb-3">
                Test Piler's features with the online demo before installing.
              </p>
              <a
                href="https://mailpiler.com/demo"
                target="_blank"
                rel="noopener noreferrer"
                class="text-primary-light dark:text-primary-dark hover:underline inline-flex items-center"
              >
                Access Demo
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                </svg>
              </a>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- CTA Section -->
    <section class="bg-primary-light dark:bg-primary-dark py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold text-white mb-6">
          Need Professional Support?
        </h2>
        <p class="text-xl text-blue-100 mb-8">
          Consider the Enterprise Edition for dedicated support, training, and consulting services.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <NuxtLink
            to="/compare"
            class="inline-block px-8 py-3 bg-white text-primary-light font-semibold rounded-lg hover:bg-gray-100 transition-colors"
          >
            Compare Editions
          </NuxtLink>
          <a
            href="https://mailpiler.com/contact"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-block px-8 py-3 bg-blue-600 dark:bg-blue-700 text-white border-2 border-white rounded-lg font-semibold hover:bg-blue-700 dark:hover:bg-blue-800 transition-colors"
          >
            Contact Enterprise Sales
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Documentation - Piler Email Archiving',
  meta: [
    { name: 'description', content: 'Complete documentation for installing, configuring, and maintaining Piler email archiving system.' }
  ]
})
</script>
