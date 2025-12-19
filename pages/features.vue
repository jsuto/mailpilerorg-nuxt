<template>
  <div>
    <!-- Hero Section -->
    <section class="bg-gradient-to-b from-blue-50 to-white dark:from-gray-800 dark:to-gray-900 py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <h1 class="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white mb-4">
            Features of Piler
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            A comprehensive email archiving solution with powerful features for compliance, security, and efficiency.
          </p>
        </div>
      </div>
    </section>

    <!-- Features Sections -->
    <section class="py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

        <!-- Archiving Features -->
        <div class="mb-16">
          <div class="flex items-center mb-8">
            <div class="text-primary-light dark:text-primary-dark mr-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8h14M5 8a2 2 0 110-4h14a2 2 0 110 4M5 8v10a2 2 0 002 2h10a2 2 0 002-2V8m-9 4h4" />
              </svg>
            </div>
            <h2 class="text-3xl font-bold text-gray-900 dark:text-white">
              Archiving
            </h2>
          </div>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <FeatureCard
              title="Built-in SMTP Server"
              description="Native SMTP server for seamless email archiving without additional infrastructure."
            />
            <FeatureCard
              title="STARTTLS Support"
              description="Secure email transmission with STARTTLS encryption support."
            />
            <FeatureCard
              title="Exclusion Rules"
              description="Configure flexible exclusion rules to control what gets archived."
            />
            <FeatureCard
              title="Retention Rules"
              description="Automated retention policies to comply with regulatory requirements."
            />
            <FeatureCard
              title="Attachment Deduplication"
              description="Intelligent deduplication saves storage space by storing attachments only once."
            />
            <FeatureCard
              title="Zlib Compression"
              description="Efficient compression reduces storage requirements while maintaining data integrity."
            />
            <FeatureCard
              title="AES-256 Encryption"
              description="Military-grade encryption ensures your archived emails remain secure."
            />
            <FeatureCard
              title="Digital Signing & Verification"
              description="Cryptographic signing and verification for tamper-proof archives."
            />
          </div>
        </div>

        <!-- Searching Features -->
        <div class="mb-16">
          <div class="flex items-center mb-8">
            <div class="text-primary-light dark:text-primary-dark mr-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
              </svg>
            </div>
            <h2 class="text-3xl font-bold text-gray-900 dark:text-white">
              Searching
            </h2>
          </div>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <FeatureCard
              title="Simple Search"
              description="Quick and intuitive search interface for finding emails fast."
            />
            <FeatureCard
              title="Advanced Search"
              description="Powerful query builder with filters for complex search requirements."
            />
            <FeatureCard
              title="Save/Load Search Criteria"
              description="Save frequently used search queries for quick access."
            />
            <FeatureCard
              title="Tagging Emails"
              description="Organize and categorize emails with custom tags."
            />
            <FeatureCard
              title="Adding Notes"
              description="Attach notes and comments to archived emails for context."
            />
            <FeatureCard
              title="View/Export/Restore"
              description="View archived emails in browser, export to various formats, or restore to mailbox."
            />
          </div>
        </div>

        <!-- Web Interface Features -->
        <div class="mb-16">
          <div class="flex items-center mb-8">
            <div class="text-primary-light dark:text-primary-dark mr-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <h2 class="text-3xl font-bold text-gray-900 dark:text-white">
              Web Interface
            </h2>
          </div>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <FeatureCard
              title="Browser-Based Access"
              description="Access your email archive from anywhere with a web browser."
            />
            <FeatureCard
              title="AD/LDAP Authentication"
              description="Integrate with Active Directory or LDAP for centralized user management."
            />
            <FeatureCard
              title="Single Sign-On"
              description="Seamless authentication with SSO support for enterprise environments."
            />
            <FeatureCard
              title="Google OAuth"
              description="Allow users to authenticate using their Google accounts."
            />
            <FeatureCard
              title="IMAP Authentication"
              description="Support for IMAP-based authentication against mail servers."
            />
            <FeatureCard
              title="POP3 Authentication"
              description="POP3 authentication support for legacy systems."
            />
            <FeatureCard
              title="2 Factor Authentication"
              description="Enhanced security with two-factor authentication (2FA) support."
            />
            <FeatureCard
              title="Custom Authentication Hooks"
              description="Flexible authentication system with support for custom hooks."
            />
            <FeatureCard
              title="Access Control"
              description="Granular permissions and access control for users and groups."
            />
            <FeatureCard
              title="Internationalization (i18n)"
              description="Multi-language support for global organizations."
            />
          </div>
        </div>

        <!-- Monitoring & Audit Features -->
        <div class="mb-16">
          <div class="flex items-center mb-8">
            <div class="text-primary-light dark:text-primary-dark mr-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
              </svg>
            </div>
            <h2 class="text-3xl font-bold text-gray-900 dark:text-white">
              Monitoring & Audit
            </h2>
          </div>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <FeatureCard
              title="Event Logging"
              description="Comprehensive logging of all system events and user actions."
            />
            <FeatureCard
              title="Audit Log Search"
              description="Search and analyze audit logs for compliance and troubleshooting."
            />
            <FeatureCard
              title="Legal Hold"
              description="Place emails under legal hold to prevent deletion during litigation."
            />
            <FeatureCard
              title="Status Info & Charts"
              description="Monitor system health with real-time status information and charts."
            />
          </div>
        </div>

        <!-- Import/Export Features -->
        <div class="mb-16">
          <div class="flex items-center mb-8">
            <div class="text-primary-light dark:text-primary-dark mr-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7H5a2 2 0 00-2 2v9a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-3m-1 4l-3 3m0 0l-3-3m3 3V4" />
              </svg>
            </div>
            <h2 class="text-3xl font-bold text-gray-900 dark:text-white">
              Import & Export
            </h2>
          </div>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <FeatureCard
              title="Export to EML"
              description="Export emails to standard EML format for compatibility with email clients."
            />
            <FeatureCard
              title="Import from EML & Mailbox"
              description="Support for importing from EML files and standard mailbox formats."
            />
            <FeatureCard
              title="Import from POP3/IMAP"
              description="Directly import emails from POP3 or IMAP accounts."
            />
          </div>
        </div>

      </div>
    </section>

    <!-- CTA Section -->
    <section class="bg-primary-light dark:bg-primary-dark py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold text-white mb-6">
          Ready to Experience These Features?
        </h2>
        <p class="text-xl text-blue-100 mb-8">
          Download Piler today and discover why it's the trusted email archiving solution.
        </p>
        <a
          href="https://github.com/jsuto/piler/"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-block px-8 py-3 bg-white text-primary-light font-semibold rounded-lg hover:bg-gray-100 transition-colors"
        >
          Download Piler
        </a>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Features - Piler Email Archiving',
  meta: [
    { name: 'description', content: 'Explore the comprehensive features of Piler email archiving solution including SMTP server, encryption, advanced search, and compliance tools.' }
  ]
})
</script>
