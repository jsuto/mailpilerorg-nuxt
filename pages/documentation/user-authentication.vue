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
            User authentication
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            To configure user authentication from external sources, eg. LDAP, AD, Zimbra, IMAP, etc. sources, set either of the following options in config-site.php.
          </p>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <!-- Placeholder Sections -->
        <div class="space-y-8">

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Authenticating against an IMAP server</h3>
            </div>
            <div class="p-6">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
		  <p>$config['ENABLE_IMAP_AUTH'] = 1;</p>
                  <p>$config['IMAP_HOST'] = 'mail.yourdomain.com';</p>
                  <p>$config['IMAP_PORT'] =  993;</p>
                  <p>$config['IMAP_SSL'] = true;</p>
                </code>
              </div>

	      <p class="text-gray-700 dark:text-gray-300 mb-4">The UI will forward authentication requests to the IMAP server. If you need auditor or additional admin users, then create them manually in the gui as local users.</p>
              <p class="text-gray-700 dark:text-gray-300 mb-4">If your IMAP server expects only usernames and not complete email addresses as the login name, then you may use a custom authentication to fix it.</p>
            </div>
          </div>


          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Authenticating against a POP3 server</h3>
            </div>
            <div class="p-6">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>$config['ENABLE_POP3_AUTH'] = 1;</p>
                  <p>$config['POP3_HOST'] = 'mail.yourdomain.com';</p>
                  <p>$config['POP3_PORT'] =  993;</p>
                  <p>$config['POP3_SSL'] = true;</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4">The same notes at the IMAP authentication above also apply here.</p>
            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Authenticating against an AD server</h3>
            </div>

            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
			    <p class="text-gray-700 dark:text-gray-300 mb-4">Create a "helper account" in your ActiveDirectory that will be used for authorization, e.g. piler@example.com</p>
		        <p class="text-gray-700 dark:text-gray-300 mb-4">Export the certificate used by your AD server as "Base64 encoded X.509 (.CER)" and copy it to "/usr/local/share/ca-certificates/" with a ".crt" extension, then run "update-ca-certificates" (Debian)</p>
    		    <p class="text-gray-700 dark:text-gray-300 mb-4">Test with <pre>ldapsearch -H ldaps://yourserver.example.com:636 -x -D "piler" -W -b 'OU=Users,DC=example,DC=com'</pre></p>
			  </div>
			</div>
				
            <div class="p-6">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>$config['ENABLE_LDAP_AUTH'] = 1;</p>
                  <p>$config['LDAP_USE_START_TLS'] = 1;</p>
                  <p>$config['LDAP_HOST'] = 'ad.example.com';</p>
                  <p>$config['LDAP_MAIL_ATTR'] = 'proxyAddresses';</p>
                  <p>$config['LDAP_ACCOUNT_OBJECTCLASS'] = 'user';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_OBJECTCLASS'] = 'group';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_ATTR'] = 'member';</p>
                  <p>$config['LDAP_HELPER_DN'] = 'cn=.....';</p>
                  <p>$config['LDAP_HELPER_PASSWORD'] = 'xxxxxxx';</p>
                </code>
              </div>
            
              <p class="text-gray-700 dark:text-gray-300 mb-4"></p>
            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Authenticating against a Zimbra server</h3>
            </div>
            <div class="p-6">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>$config['ENABLE_LDAP_AUTH'] = 1;</p>
                  <p>$config['LDAP_USE_START_TLS'] = 1;</p>
                  <p>$config['LDAP_HOST'] = 'zimbra.example.com';</p>
                  <p>$config['LDAP_MAIL_ATTR'] = 'mail';</p>
                  <p>$config['LDAP_ACCOUNT_OBJECTCLASS'] = 'zimbraAccount';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_OBJECTCLASS'] = 'zimbraDistributionList';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_ATTR'] = 'zimbraMailForwardingAddress';</p>
                  <p>$config['LDAP_HELPER_DN'] = 'uid=zimbra,cn=admins,cn=zimbra';</p>
                  <p>$config['LDAP_HELPER_PASSWORD'] = 'xxxxxxx';</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4"></p>
            </div>
          </div>


          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Authenticating against Lotus Domino</h3>
            </div>
            <div class="p-6">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>$config['ENABLE_LDAP_AUTH'] = 1;</p>
                  <p>$config['LDAP_USE_START_TLS'] = 1;</p>
                  <p>$config['LDAP_MAIL_ATTR'] = 'mail';</p>
                  <p>$config['LDAP_ACCOUNT_OBJECTCLASS'] = 'dominoPerson';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_OBJECTCLASS'] = 'dominoGroup');</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_ATTR'] = 'mail';</p>
                  <p>$config['LDAP_HELPER_DN'] = '.........';</p>
                  <p>$config['LDAP_HELPER_PASSWORD'] = 'xxxxxxx';</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4"></p>
            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Authenticating against iredmail</h3>
            </div>
            <div class="p-6">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>$config['ENABLE_LDAP_AUTH'] = 1;</p>
                  <p>$config['LDAP_USE_START_TLS'] = 1;</p>
                  <p>$config['LDAP_MAIL_ATTR'] = 'mail';</p>
                  <p>$config['LDAP_ACCOUNT_OBJECTCLASS'] = 'mailUser';</p>
                  <p>$config['LDAP_BASE_DN'] = 'o=domains,dc=yourdomain,dc=com';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_OBJECTCLASS'] = 'mailList';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_ATTR'] = 'memberOfGroup';</p>
                  <p>$config['LDAP_HELPER_DN'] = 'cn=vmailadmin,dc=yourdomain,dc=com';</p>
                  <p>$config['LDAP_HELPER_PASSWORD'] = 'xxxxxxx';</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4"></p>
            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Authenticating against Univention</h3>
            </div>
            <div class="p-6">
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>$config['ENABLE_LDAP_AUTH'] = 1;</p>
                  <p>$config['LDAP_USE_START_TLS'] = 1;</p>
                  <p>$config['LDAP_HOST'] = 'univention.example.com';</p>
                  <p>$config['LDAP_MAIL_ATTR'] = 'mailPrimaryAddress';</p>
                  <p>$config['LDAP_ACCOUNT_OBJECTCLASS'] = 'person';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_OBJECTCLASS'] = 'person';</p>
                  <p>$config['LDAP_DISTRIBUTIONLIST_ATTR'] = 'mailAlternativeAddress';</p>
                  <p>$config['LDAP_HELPER_DN'] = '.........';</p>
                  <p>$config['LDAP_HELPER_PASSWORD'] = 'xxxxxxx';</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4"></p>
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
