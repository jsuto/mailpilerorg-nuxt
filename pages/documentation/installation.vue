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
            Installation
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Step-by-step guide to install Piler on your server, including system requirements and dependencies.
          </p>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <div class="space-y-8">

          <!-- System Requirements -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">System Requirements</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300">2+ CPU cores</p>
              <p class="text-gray-700 dark:text-gray-300">2+ GB memory</p>
              <p class="text-gray-700 dark:text-gray-300">200+ GB disk</p>
            </div>
          </div>

          <!-- Dependencies -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Install Dependencies</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Required packages and dependencies</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                <code class="text-green-400 text-sm font-mono">
		  <p>apt-get update</p>
                  <p>apt-get -y --no-install-recommends install sysstat wget openssl sysstat php-cli php-cgi php-mysql \</p>
                  <p>&nbsp;&nbsp;&nbsp;make gcc libssl-dev libtre-dev libzip-dev libmariadb-dev libcurl4-openssl-dev \</p>
                  <p>&nbsp;&nbsp;&nbsp;php-fpm php-zip php-ldap php-gd php-curl php-xml php-memcached catdoc unrtf poppler-utils \</p>
                  <p>&nbsp;&nbsp;&nbsp;nginx tnef sudo libzip4t64 libtre5 cron mariadb-server mariadb-client-core python3 python3-mysqldb \</p>
                  <p>&nbsp;&nbsp;&nbsp;ca-certificates curl rsyslog gnupg</p>

		  <p>wget https://repo.manticoresearch.com/manticore-repo.noarch.deb</p>
		  <p>dpkg -i manticore-repo.noarch.deb</p>
		  <p>apt-get update && apt-get install -y manticore manticore-columnar-lib manticore-extra</p>
	   	  <p>rm -f manticore-repo.noarch.deb</p>
		  <p>systemctl stop manticore</p>
		  <p>systemctl disable manticore</p>
                </code>
              </div>
            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Download & Install Piler</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Create a dedicated and non-privileged user to run piler</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mb-4 p-4">
	        <code class="text-green-400 text-sm font-mono">
		  <p>groupadd piler</p>
                  <p>useradd -g piler -m -s /bin/bash -d /var/piler piler</p>
                  <p>usermod -L piler</p>
                  <p>chmod 755 /var/piler</p>
	        </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4">Unpack and compile piler</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>tar zxvf piler-x.y.z.tar.gz</p>
                  <p>cd piler-x.y.z</p>
                  <p>./configure --localstatedir=/var --with-database=mysql</p>
                  <p>make</p>
                  <p>sudo make install</p>
                  <p>ldconfig</p>
                </code>
              </div>

            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Postinstall tasks</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300">Piler requires bootstrapping the database, creating cron entries, etc.</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mt-4 mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>/usr/local/libexec/piler/postinstall.sh</p>
                </code>
              </div>

              <p class="text-gray-700 dark:text-gray-300">Setup systemd services</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mt-4 mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">
                  <p>pushd /etc/systemd/system</p>
                  <p>ln -sf /usr/local/libexec/piler/piler.service</p>
                  <p>ln -sf /usr/local/libexec/piler/piler-smtp.service</p>
                  <p>ln -sf /usr/local/libexec/piler/pilersearch.service</p>
                  <p>systemctl daemon-reload</p>
                  <p>systemctl enable --now piler</p>
                  <p>systemctl enable --now piler-smtp</p>
                  <p>systemctl enable --now pilersearch</p>
		  <p>popd</p>
                </code>
              </div>

            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Configure your mail server</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300">
		<NuxtLink to="/documentation/configure-mail-server" class="text-primary-light dark:text-primary-dark hover:underline mb-4 inline-flex items-center text-sm font-medium">
        	  Configure your mail server
        	</NuxtLink> to pass a copy of each received email to the archive over smtp
              </p>
            </div>
          </div>

          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">Configure the web UI</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Create a virtualhost dedicated to piler, and enable rewriting rules. Example webserver configurations are available in the contrib/webserver/ directory.</p>

	      <p class="text-gray-700 dark:text-gray-300 mb-4">Log in as administrator using the following account:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg mt-4 mb-4 p-4">
                <code class="text-green-400 text-sm font-mono">admin@local:pilerrocks</code>
              </div>

              <p class="text-gray-700 dark:text-gray-300 mb-4">Add your own domains that piler will receive emails for in the Administration/Domain menu.</p>

              <p class="text-gray-700 dark:text-gray-300 mb-4">Review Administering piler / Retention rules, and set the appropriate retention rules, if needed. Otherwise piler will retain everything for ‘default_retention_days’ set in piler.conf</p>

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
