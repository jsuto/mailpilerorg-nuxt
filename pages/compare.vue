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

    <!-- Edition Pricing Headers -->
    <section class="py-10 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid md:grid-cols-2 gap-6">

          <!-- Open Source -->
          <div class="bg-white dark:bg-gray-900 rounded-lg border-2 border-gray-200 dark:border-gray-700 px-6 py-6 flex flex-col">
            <div class="mb-4">
              <h2 class="text-2xl font-bold text-gray-900 dark:text-white">Open Source Edition</h2>
              <p class="text-gray-500 dark:text-gray-400 mt-1">Free, powerful, community-driven. Single server.</p>
            </div>
            <div class="mb-6">
              <span class="text-4xl font-bold text-gray-900 dark:text-white">Free</span>
              <span class="text-gray-500 dark:text-gray-400 ml-2">forever</span>
            </div>
            <a
              href="https://github.com/jsuto/piler/"
              target="_blank"
              rel="noopener noreferrer"
              class="mt-auto block w-full px-6 py-3 bg-primary-light dark:bg-primary-dark text-white text-center rounded-lg font-semibold hover:opacity-90 transition-opacity"
            >
              Download Open Source
            </a>
          </div>

          <!-- Enterprise -->
          <div class="bg-white dark:bg-gray-900 rounded-lg border-2 border-blue-500 dark:border-blue-600 px-6 py-6 flex flex-col relative">
            <div class="absolute top-0 right-0 bg-blue-500 text-white px-4 py-1 text-sm font-semibold rounded-bl-lg">
              Professional
            </div>
            <div class="mb-4">
              <h2 class="text-2xl font-bold text-gray-900 dark:text-white">Enterprise Edition</h2>
              <p class="text-gray-500 dark:text-gray-400 mt-1">Professional support, AI features, multi-tenancy, and more.</p>
            </div>
            <div class="mb-6">
              <span class="text-4xl font-bold text-gray-900 dark:text-white">Contact</span>
              <span class="text-gray-500 dark:text-gray-400 ml-2">for pricing</span>
            </div>
            <div class="mt-auto flex flex-col sm:flex-row gap-3">
              <a
                href="https://mailpiler.com/#features"
                target="_blank"
                rel="noopener noreferrer"
                class="flex-1 px-6 py-3 bg-blue-600 dark:bg-blue-700 text-white text-center rounded-lg font-semibold hover:bg-blue-700 dark:hover:bg-blue-800 transition-colors"
              >
                Learn More
              </a>
              <a
                href="https://mailpiler.com/contact"
                target="_blank"
                rel="noopener noreferrer"
                class="flex-1 px-6 py-3 bg-white dark:bg-gray-800 text-gray-900 dark:text-white text-center border-2 border-gray-300 dark:border-gray-600 rounded-lg font-semibold hover:bg-gray-50 dark:hover:bg-gray-700 transition-colors"
              >
                Contact Sales
              </a>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- Feature Comparison Table -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center text-gray-900 dark:text-white mb-12">
          Feature Comparison
        </h2>
        <div class="overflow-x-auto rounded-lg border border-gray-200 dark:border-gray-700">
          <table class="w-full text-sm">
            <thead>
              <tr class="bg-gray-50 dark:bg-gray-800">
                <th class="text-left px-6 py-4 font-semibold text-gray-700 dark:text-gray-300 w-1/2">Feature</th>
                <th class="text-center px-6 py-4 font-semibold text-gray-700 dark:text-gray-300">Open Source</th>
                <th class="text-center px-6 py-4 font-semibold text-blue-600 dark:text-blue-400">Enterprise</th>
              </tr>
            </thead>
            <tbody class="divide-y divide-gray-100 dark:divide-gray-800">
              <!-- Archiving -->
              <tr class="bg-gray-50 dark:bg-gray-800/50">
                <td colspan="3" class="px-6 py-2 text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-gray-400">Archiving</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Email archiving via SMTP</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Google Apps &amp; Office 365 ingestion</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">MS Teams archiving</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Import/export (EML, MBOX, IMAP, POP3)</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">AES-256 encryption</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Deduplication &amp; compression</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>

              <!-- Search -->
              <tr class="bg-gray-50 dark:bg-gray-800/50">
                <td colspan="3" class="px-6 py-2 text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-gray-400">Search</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Full-text search</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Semantic (AI-powered) search</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>

              <!-- Compliance & Governance -->
              <tr class="bg-gray-50 dark:bg-gray-800/50">
                <td colspan="3" class="px-6 py-2 text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-gray-400">Compliance &amp; Governance</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Retention &amp; exclusion rules</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Legal hold &amp; audit logs</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">eDiscovery support</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Smart Insights (sensitive data detection)</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">SIEM integration</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>

              <!-- Authentication -->
              <tr class="bg-gray-50 dark:bg-gray-800/50">
                <td colspan="3" class="px-6 py-2 text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-gray-400">Authentication</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">AD/LDAP, Google OAuth2, 2FA</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">NTLM/Kerberos SSO</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">SAML 2.0 (Azure AD, Google Workspace)</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">OAuth2 SSO (Azure AD, Google Workspace)</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Passkeys (WebAuthn)</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>

              <!-- Infrastructure -->
              <tr class="bg-gray-50 dark:bg-gray-800/50">
                <td colspan="3" class="px-6 py-2 text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-gray-400">Infrastructure</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Single-server deployment</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Multi-node scale-out</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">S3 object storage</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Multi-tenancy</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>

              <!-- Management -->
              <tr class="bg-gray-50 dark:bg-gray-800/50">
                <td colspan="3" class="px-6 py-2 text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-gray-400">Management &amp; Visibility</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">REST API</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Analytics dashboard</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Permission profiles</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Observability (logs, metrics, traces)</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>

              <!-- Support -->
              <tr class="bg-gray-50 dark:bg-gray-800/50">
                <td colspan="3" class="px-6 py-2 text-xs font-semibold uppercase tracking-wider text-gray-500 dark:text-gray-400">Support</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Community forums &amp; documentation</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Professional support with guaranteed response times</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Implementation &amp; onboarding assistance</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
              <tr class="hover:bg-gray-50 dark:hover:bg-gray-800/30">
                <td class="px-6 py-3 text-gray-700 dark:text-gray-300">Custom development</td>
                <td class="px-6 py-3 text-center text-gray-300 dark:text-gray-600">—</td>
                <td class="px-6 py-3 text-center text-green-500">✓</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </section>

    <!-- Compliance Section -->
    <section class="py-16 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center text-gray-900 dark:text-white mb-4">
          Built for Regulatory Compliance
        </h2>
        <p class="text-center text-gray-600 dark:text-gray-400 mb-10 max-w-2xl mx-auto">
          Both editions support key compliance requirements. The Enterprise Edition adds deeper tooling for regulated industries.
        </p>
        <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
          <div class="bg-white dark:bg-gray-900 rounded-lg p-5 border border-gray-200 dark:border-gray-700 text-center">
            <div class="text-2xl font-bold text-blue-600 dark:text-blue-400 mb-2">GDPR</div>
            <p class="text-sm text-gray-600 dark:text-gray-400">Retention policies, data subject access, audit trails</p>
          </div>
          <div class="bg-white dark:bg-gray-900 rounded-lg p-5 border border-gray-200 dark:border-gray-700 text-center">
            <div class="text-2xl font-bold text-blue-600 dark:text-blue-400 mb-2">SOX</div>
            <p class="text-sm text-gray-600 dark:text-gray-400">Tamper-proof archiving, legal hold, audit logs</p>
          </div>
          <div class="bg-white dark:bg-gray-900 rounded-lg p-5 border border-gray-200 dark:border-gray-700 text-center">
            <div class="text-2xl font-bold text-blue-600 dark:text-blue-400 mb-2">HIPAA</div>
            <p class="text-sm text-gray-600 dark:text-gray-400">Encryption at rest, access controls, audit trails</p>
          </div>
          <div class="bg-white dark:bg-gray-900 rounded-lg p-5 border border-gray-200 dark:border-gray-700 text-center">
            <div class="text-2xl font-bold text-blue-600 dark:text-blue-400 mb-2">MiFID II</div>
            <p class="text-sm text-gray-600 dark:text-gray-400">Communications archiving, eDiscovery, retention rules</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Deployment Options -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center text-gray-900 dark:text-white mb-4">
          Deployment Options
        </h2>
        <p class="text-center text-gray-600 dark:text-gray-400 mb-10 max-w-2xl mx-auto">
          Deploy the way that fits your infrastructure — from a single server to a multi-tenant managed service.
        </p>
        <div class="grid md:grid-cols-3 gap-6">
          <div class="bg-gray-50 dark:bg-gray-800 rounded-lg p-6 border border-gray-200 dark:border-gray-700">
            <div class="font-semibold text-lg text-gray-900 dark:text-white mb-2">Single Server</div>
            <div class="text-xs font-medium text-green-600 dark:text-green-400 mb-3">Open Source &amp; Enterprise</div>
            <p class="text-sm text-gray-600 dark:text-gray-400">One server handles archiving, search, and the web UI. Ideal for small to mid-size organizations.</p>
          </div>
          <div class="bg-gray-50 dark:bg-gray-800 rounded-lg p-6 border border-gray-200 dark:border-gray-700">
            <div class="font-semibold text-lg text-gray-900 dark:text-white mb-2">Multi-Node Scale-Out</div>
            <div class="text-xs font-medium text-blue-600 dark:text-blue-400 mb-3">Enterprise only</div>
            <p class="text-sm text-gray-600 dark:text-gray-400">Distribute load across multiple nodes with S3 object storage for high-volume or high-availability deployments.</p>
          </div>
          <div class="bg-gray-50 dark:bg-gray-800 rounded-lg p-6 border border-gray-200 dark:border-gray-700">
            <div class="font-semibold text-lg text-gray-900 dark:text-white mb-2">Multi-Tenant (MSP)</div>
            <div class="text-xs font-medium text-blue-600 dark:text-blue-400 mb-3">Enterprise only</div>
            <p class="text-sm text-gray-600 dark:text-gray-400">Serve multiple independent organizations from one installation — ideal for managed service providers and cloud offerings.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Decision Guide -->
    <section class="py-16 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center text-gray-900 dark:text-white mb-12">
          Which Edition Is Right for You?
        </h2>

        <div class="grid md:grid-cols-2 gap-8">
          <!-- Open Source Use Cases -->
          <div class="bg-white dark:bg-gray-900 p-6 rounded-lg border border-gray-200 dark:border-gray-700">
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
                <span>Operate in a regulated industry (finance, healthcare, legal)</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Are an MSP providing archiving to multiple clients</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Need high-availability or large-scale deployments</span>
              </li>
              <li class="flex items-start">
                <svg class="h-5 w-5 text-blue-600 dark:text-blue-400 mr-2 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Require implementation assistance and training</span>
              </li>
            </ul>
          </div>
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
