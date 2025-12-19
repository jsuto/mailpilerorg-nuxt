<template>
  <div>
    <!-- Hero Section -->
    <section class="bg-gradient-to-b from-blue-50 to-white dark:from-gray-800 dark:to-gray-900 py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <h1 class="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white mb-4">
            Choose the Right Edition
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Both editions offer powerful email archiving. Choose based on your organization's needs and resources.
          </p>
        </div>
      </div>
    </section>

    <!-- Intro Section -->
    <section class="py-12 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="prose prose-lg dark:prose-invert max-w-none">
          <p class="text-lg text-gray-700 dark:text-gray-300 text-center">
            Piler is available in two editions: the <strong>Open Source Edition</strong> (free and community-supported)
            and the <strong>Enterprise Edition</strong> (with professional support and additional features).
            Both provide robust email archiving capabilities—choose the one that fits your organization best.
          </p>
        </div>
      </div>
    </section>

    <!-- Comparison Cards -->
    <section class="py-16 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid lg:grid-cols-2 gap-8 mb-12">

          <!-- Open Source Edition Card -->
          <div class="bg-white dark:bg-gray-900 rounded-lg shadow-xl border-2 border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-8 text-white">
              <h2 class="text-3xl font-bold mb-2">Open Source Edition</h2>
              <p class="text-blue-100 text-lg">Free, powerful, community-driven</p>
              <div class="mt-4">
                <span class="text-4xl font-bold">Free</span>
                <span class="text-blue-100 ml-2">Forever</span>
              </div>
            </div>
            <div class="px-6 py-8">
              <p class="text-gray-600 dark:text-gray-400 mb-6">
                Perfect for organizations that want full control, have technical expertise, and prefer community support.
              </p>

              <h3 class="font-semibold text-lg text-gray-900 dark:text-white mb-4">What's Included:</h3>
              <ul class="space-y-3 mb-8">
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Full archiving capabilities with SMTP server</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">AES-256 encryption & virus checking</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Advanced search & full-text indexing</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Retention & exclusion rules</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Legal hold & audit logs</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Deduplication & compression</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Web GUI with AD/LDAP, SSO, OAuth, 2FA</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Google Apps & Office 365 support</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Import/export (PST, EML, IMAP, POP3)</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Community support & documentation</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-green-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Full source code access</span>
                </li>
              </ul>

              <div class="space-y-3">
                <a
                  href="https://github.com/jsuto/piler/"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="block w-full px-6 py-3 bg-primary-light dark:bg-primary-dark text-white text-center rounded-lg font-semibold hover:opacity-90 transition-opacity"
                >
                  Download Open Source
                </a>
                <a
                  href="https://demo.mailpiler.org"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="block w-full px-6 py-3 bg-white dark:bg-gray-800 text-gray-900 dark:text-white text-center border-2 border-gray-300 dark:border-gray-600 rounded-lg font-semibold hover:bg-gray-50 dark:hover:bg-gray-700 transition-colors"
                >
                  Try Online Demo
                </a>
              </div>
            </div>
          </div>

          <!-- Enterprise Edition Card -->
          <div class="bg-white dark:bg-gray-900 rounded-lg shadow-xl border-2 border-blue-500 dark:border-blue-600 overflow-hidden relative">
            <div class="absolute top-0 right-0 bg-blue-500 text-white px-4 py-1 text-sm font-semibold rounded-bl-lg">
              Professional
            </div>
            <div class="bg-gradient-to-r from-blue-600 to-blue-700 dark:from-blue-700 dark:to-blue-800 px-6 py-8 text-white">
              <h2 class="text-3xl font-bold mb-2">Enterprise Edition</h2>
              <p class="text-blue-100 text-lg">Professional support & AI-powered features</p>
              <div class="mt-4">
                <span class="text-4xl font-bold">Contact</span>
                <span class="text-blue-100 ml-2">for pricing</span>
              </div>
            </div>
            <div class="px-6 py-8">
              <p class="text-gray-600 dark:text-gray-400 mb-6">
                Ideal for organizations that need professional support, SLAs, AI-powered features, and enterprise-grade management tools.
              </p>

              <h3 class="font-semibold text-lg text-gray-900 dark:text-white mb-4">Everything in Open Source, plus:</h3>
              <ul class="space-y-3 mb-8">
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>AI-Powered Intelligence:</strong> On-premise AI for enhanced email analysis</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Professional Support:</strong> Priority email & phone support with SLA</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Dedicated Support Team:</strong> Direct access to Piler experts</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Advanced Features:</strong> Enterprise-specific capabilities</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Guaranteed Updates:</strong> Regular security patches & updates</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Implementation Assistance:</strong> Help with setup & configuration</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Training & Onboarding:</strong> User and admin training sessions</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Custom Development:</strong> Tailored features for your needs</span>
                </li>
                <li class="flex items-start">
                  <svg class="h-6 w-6 text-blue-500 mr-3 flex-shrink-0 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><strong>Compliance Consulting:</strong> Expert guidance on regulations</span>
                </li>
              </ul>

              <div class="space-y-3">
                <a
                  href="https://mailpiler.com"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="block w-full px-6 py-3 bg-blue-600 dark:bg-blue-700 text-white text-center rounded-lg font-semibold hover:bg-blue-700 dark:hover:bg-blue-800 transition-colors"
                >
                  Learn More About Enterprise
                </a>
                <a
                  href="https://mailpiler.com#contact"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="block w-full px-6 py-3 bg-white dark:bg-gray-800 text-gray-900 dark:text-white text-center border-2 border-gray-300 dark:border-gray-600 rounded-lg font-semibold hover:bg-gray-50 dark:hover:bg-gray-700 transition-colors"
                >
                  Contact Sales
                </a>
              </div>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- Decision Guide -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center text-gray-900 dark:text-white mb-12">
          Which Edition Is Right for You?
        </h2>

        <div class="grid md:grid-cols-2 gap-8">
          <!-- Open Source Use Cases -->
          <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-lg border border-gray-200 dark:border-gray-700">
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">
              Choose Open Source if you:
            </h3>
            <ul class="space-y-3 text-gray-700 dark:text-gray-300">
              <li class="flex items-start">
                <svg class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Have in-house technical expertise</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Want full control over your infrastructure</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Prefer community-driven development</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Need to minimize costs</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Want to customize and extend the platform</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-primary-light dark:text-primary-dark mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Are comfortable with self-support</span>
              </li>
            </ul>
          </div>

          <!-- Enterprise Use Cases -->
          <div class="bg-blue-50 dark:bg-blue-900/20 p-6 rounded-lg border border-blue-200 dark:border-blue-700">
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">
              Choose Enterprise if you:
            </h3>
            <ul class="space-y-3 text-gray-700 dark:text-gray-300">
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Need professional support and SLAs</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Want AI-powered email intelligence features</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Require implementation assistance</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Need guaranteed response times</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Want training and onboarding services</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Prefer vendor accountability</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Migration Path -->
    <section class="py-16 bg-gradient-to-r from-blue-50 to-indigo-50 dark:from-gray-800 dark:to-gray-700">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-6">
          Start with Open Source, Upgrade When Ready
        </h2>
        <p class="text-lg text-gray-700 dark:text-gray-300 mb-8 max-w-3xl mx-auto">
          Many organizations begin with the Open Source Edition to prove value and later upgrade to
          Enterprise as their needs grow. There's no pressure—use what works best for your organization.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="https://github.com/jsuto/piler/"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-block px-8 py-3 bg-primary-light dark:bg-primary-dark text-white rounded-lg font-semibold hover:opacity-90 transition-opacity"
          >
            Try Open Source First
          </a>
          <a
            href="https://mailpiler.com#contact"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-block px-8 py-3 bg-white dark:bg-gray-800 text-gray-900 dark:text-white border-2 border-gray-300 dark:border-gray-600 rounded-lg font-semibold hover:bg-gray-50 dark:hover:bg-gray-700 transition-colors"
          >
            Discuss Enterprise Needs
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Compare Editions - Piler Email Archiving',
  meta: [
    { name: 'description', content: 'Compare Piler Open Source and Enterprise editions. Choose the email archiving solution that fits your organization.' }
  ]
})
</script>
