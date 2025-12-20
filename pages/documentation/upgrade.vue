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
            Upgrade Instructions
          </h1>
          <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
            Safely upgrade your Piler installation to a newer version with complete step-by-step instructions.
          </p>
        </div>
      </div>
    </section>

    <!-- Important Warning -->
    <section class="py-8 bg-gray-50 dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border-l-4 border-red-500 p-8">
          <div class="flex items-start">
            <div class="flex-shrink-0">
              <div class="w-12 h-12 bg-gray-100 dark:bg-gray-700 rounded-full flex items-center justify-center">
                <svg class="h-6 w-6 text-red-600 dark:text-red-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
                </svg>
              </div>
            </div>
            <div class="ml-4">
              <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">
                Critical: Backup Before Upgrading
              </h3>
              <p class="text-gray-700 dark:text-gray-300 mb-3">
                It's strongly recommended to backup your configs including piler.key, piler.conf, piler.pem, sphinx.conf and config-site.php before the upgrade.
              </p>
              <div class="bg-gray-100 dark:bg-gray-700 rounded-lg p-4">
                <p class="text-sm font-medium text-gray-900 dark:text-gray-200 mb-2">
                  Essential files to backup:
                </p>
                <div class="flex flex-wrap gap-2 mt-2">
                  <code class="bg-gray-200 dark:bg-gray-600 text-gray-800 dark:text-gray-200 px-3 py-1 rounded text-sm font-mono">piler.key</code>
                  <code class="bg-gray-200 dark:bg-gray-600 text-gray-800 dark:text-gray-200 px-3 py-1 rounded text-sm font-mono">piler.conf</code>
                  <code class="bg-gray-200 dark:bg-gray-600 text-gray-800 dark:text-gray-200 px-3 py-1 rounded text-sm font-mono">piler.pem</code>
                  <code class="bg-gray-200 dark:bg-gray-600 text-gray-800 dark:text-gray-200 px-3 py-1 rounded text-sm font-mono">sphinx.conf</code>
                  <code class="bg-gray-200 dark:bg-gray-600 text-gray-800 dark:text-gray-200 px-3 py-1 rounded text-sm font-mono">config-site.php</code>
                </div>
              </div>
              <p class="text-sm text-gray-600 dark:text-gray-400 mt-3">
                When upgrading across multiple versions, apply all intermediate database scripts sequentially.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <section class="py-16 bg-white dark:bg-gray-900">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-3">
            Version-Specific Upgrade Paths
          </h2>
          <p class="text-lg text-gray-600 dark:text-gray-400">
            Follow the instructions for your version upgrade path
          </p>
        </div>

        <div class="space-y-8">

          <!-- 0.1.18 → 0.1.19 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">0.1.18 → 0.1.19</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4 mb-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-0.18-vs-0.19.sql</code>
              </div>
              <p class="text-gray-700 dark:text-gray-300 mb-3">Add the following variables to config.php:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                <pre class="text-green-400 text-sm font-mono"><code>define('TABLE_GROUP', 'group');
define('TABLE_GROUP_USER', 'group_user');
define('TABLE_GROUP_EMAIL', 'group_email');</code></pre>
              </div>
            </div>
          </div>

          <!-- 0.1.19 → 0.1.20 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">0.1.19 → 0.1.20</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-0.19-vs-0.20.sql</code>
              </div>
            </div>
          </div>

          <!-- 0.1.20 → 0.1.21 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border-2 border-yellow-400 dark:border-yellow-500 overflow-hidden">
            <div class="bg-gradient-to-r from-yellow-500 to-yellow-600 dark:from-yellow-600 dark:to-yellow-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white flex items-center">
                0.1.20 → 0.1.21
                <span class="ml-3 text-sm bg-white/20 px-3 py-1 rounded-full">⚠️ Breaking Changes</span>
              </h3>
            </div>
            <div class="p-6">
              <div class="bg-yellow-50 dark:bg-yellow-900/20 border-l-4 border-yellow-500 p-4 mb-4">
                <p class="font-semibold text-yellow-900 dark:text-yellow-200 mb-2">⚠️ Important Warning</p>
                <p class="text-yellow-800 dark:text-yellow-300 text-sm">Backup the 'tag' and 'note' tables, then drop them. The new version has a modified schema.</p>
              </div>
              <p class="text-gray-700 dark:text-gray-300 mb-3">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4 mb-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-0.20-vs-0.21.sql</code>
              </div>
              <p class="text-gray-700 dark:text-gray-300 mb-3">Add the following to config.php:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                <pre class="text-green-400 text-sm font-mono"><code>define('TABLE_FOLDER', 'folder');
define('TABLE_FOLDER_RULE', 'folder_rule');
define('TABLE_FOLDER_MESSAGE', 'folder_message');
define('TABLE_FOLDER_EXTRA', 'folder_extra');
define('TABLE_NOTE', 'note');
define('ICON_FOLDER', 'images/folder.png');
define('ICON_EMPTY_FOLDER', 'images/folder-open.png');</code></pre>
              </div>
            </div>
          </div>

          <!-- 0.1.21 → 0.1.22 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">0.1.21 → 0.1.22</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4 mb-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-0.21-vs-0.22.sql</code>
              </div>
              <div class="space-y-4">
                <div>
                  <p class="text-gray-700 dark:text-gray-300 mb-2">Rename in config.php:</p>
                  <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                    <code class="text-green-400 text-sm font-mono">LANG → DEFAULT_LANG</code>
                  </div>
                </div>
                <div>
                  <p class="text-gray-700 dark:text-gray-300 mb-2">Add the following to config.php:</p>
                  <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                    <pre class="text-green-400 text-sm font-mono"><code>$config['MEMCACHED_ENABLED'] = 0;
$config['MEMCACHED_PREFIX'] = 'piler';
$config['MEMCACHED_TTL'] = 86400;
$config['TIMEZONE'] = 'Europe/Budapest';
$config['DB_CHARSET'] = 'utf8';
$config['ENABLE_DELETE'] = 1;</code></pre>
                  </div>
                </div>
                <div>
                  <p class="text-gray-700 dark:text-gray-300 mb-2">Update search indices:</p>
                  <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                    <pre class="text-green-400 text-sm font-mono"><code>searchd stop
indexer --config /etc/piler/sphinx.conf note1
searchd start</code></pre>
                  </div>
                </div>
                <div>
                  <p class="text-gray-700 dark:text-gray-300">Remove folder related lines from sphinx.conf</p>
                </div>
              </div>
            </div>
          </div>

          <!-- 0.1.22 → 0.1.23 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">0.1.22 → 0.1.23</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4 mb-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-0.1.22-vs-0.1.23.sql</code>
              </div>
              <p class="text-gray-700 dark:text-gray-300 mb-3">Restructure the store directory:</p>
              <p class="text-gray-700 dark:text-gray-300">From: <code class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded text-sm">$localstatedir/piler/store/</code></p>
              <p class="text-gray-700 dark:text-gray-300">To: <code class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded text-sm">$localstatedir/piler/store/&lt;SERVER_ID&gt;</code></p>
            </div>
          </div>

          <!-- 0.1.23 → 0.1.24 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">0.1.23 → 0.1.24</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4 mb-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-0.1.23-vs-0.1.24.sql</code>
              </div>
              <p class="text-gray-700 dark:text-gray-300">Update sphinx indexing scheme and cron jobs to new delta-delta structure.</p>
            </div>
          </div>

          <!-- 0.1.24 → 1.1.0 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">0.1.24 → 1.1.0</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-0.1.24-vs-1.1.0.sql</code>
              </div>
            </div>
          </div>

          <!-- 1.1.1 → 1.2.0 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">1.1.1 → 1.2.0</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4">Execute the following sql script on the piler database:</p>
              <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4 mb-4">
                <code class="text-green-400 text-sm font-mono">mysql -u piler -p piler &lt; util/db-upgrade-1.1.0-vs-1.2.0.sql</code>
              </div>
              <div class="bg-blue-50 dark:bg-blue-900/20 border-l-4 border-blue-500 p-4">
                <p class="text-blue-900 dark:text-blue-200 text-sm">
                  <strong>Note:</strong> All piler related configs moved to ${sysconfdir}/piler directory.
                </p>
              </div>
            </div>
          </div>

          <!-- 1.2.0 → 1.3.0 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">1.2.0 → 1.3.0</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300">No additional steps required.</p>
            </div>
          </div>

          <!-- 1.3.0 → 1.3.5 -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-blue-500 to-blue-600 dark:from-blue-600 dark:to-blue-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">1.3.0 → 1.3.5</h3>
            </div>
            <div class="p-6">
              <p class="text-gray-700 dark:text-gray-300 mb-4"><strong>Optional:</strong> Upgrade MySQL encoding from utf8 to utf8mb4 for complete UTF-8 support (including emojis).</p>
              <p class="text-gray-700 dark:text-gray-300">Alternatively, maintain current settings with specific charset configurations in three configuration files and execute ALTER TABLE statements.</p>
            </div>
          </div>

          <!-- 1.4.5 → 1.4.6 (Docker) -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-indigo-500 to-indigo-600 dark:from-indigo-600 dark:to-indigo-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">1.4.5 → 1.4.6 <span class="text-sm font-normal text-indigo-100">(Docker)</span></h3>
            </div>
            <div class="p-6 space-y-4">
              <div>
                <p class="text-gray-700 dark:text-gray-300 mb-3">Update file ownership:</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono">chown -R 1001:1001 &lt;volume_folder&gt;</code>
                </div>
              </div>
              <div>
                <p class="text-gray-700 dark:text-gray-300">Add audit1 index to manticore.conf</p>
              </div>
              <div>
                <p class="text-gray-700 dark:text-gray-300">Update PHP version to 8.3 in nginx configuration</p>
              </div>
            </div>
          </div>

          <!-- 1.4.6 → 1.4.7 (Docker) -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700 overflow-hidden">
            <div class="bg-gradient-to-r from-indigo-500 to-indigo-600 dark:from-indigo-600 dark:to-indigo-700 px-6 py-4">
              <h3 class="text-xl font-bold text-white">1.4.6 → 1.4.7 <span class="text-sm font-normal text-indigo-100">(Docker)</span></h3>
            </div>
            <div class="p-6 space-y-4">
              <div class="bg-blue-50 dark:bg-blue-900/20 border-l-4 border-blue-500 p-4 mb-4">
                <p class="text-blue-900 dark:text-blue-200 text-sm">
                  <strong>Note:</strong> Manticore index is moved to a separate container.
                </p>
              </div>
              <div>
                <p class="text-gray-700 dark:text-gray-300 mb-3">Add manticore service to docker-compose.yaml</p>
              </div>
              <div>
                <p class="text-gray-700 dark:text-gray-300 mb-3">Adjust piler service with environment variable:</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono">MANTICORE_HOSTNAME=manticore</code>
                </div>
              </div>
              <div>
                <p class="text-gray-700 dark:text-gray-300 mb-3">Update ownership:</p>
                <div class="bg-gray-900 dark:bg-gray-950 rounded-lg p-4">
                  <code class="text-green-400 text-sm font-mono">chown -R 999:999 &lt;manticore_volume&gt;</code>
                </div>
              </div>
              <div>
                <p class="text-gray-700 dark:text-gray-300">Configure hostname settings in piler.conf and config-site.php</p>
              </div>
            </div>
          </div>

        </div>

        <!-- GUI Upgrade -->
        <div class="mt-16">
          <div class="text-center mb-8">
            <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-3">
              Web UI Upgrade
            </h2>
            <p class="text-lg text-gray-600 dark:text-gray-400">
              Simple and straightforward web interface updates
            </p>
          </div>
          <div class="bg-gradient-to-br from-green-50 to-green-100 dark:from-gray-800 dark:to-gray-700 rounded-xl shadow-lg border-2 border-green-400 dark:border-green-600 p-8">
            <div class="flex items-start">
              <div class="flex-shrink-0">
                <div class="w-12 h-12 bg-green-500 dark:bg-green-600 rounded-lg flex items-center justify-center">
                  <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
              </div>
              <div class="ml-4">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">
                  Simple UI Updates
                </h3>
                <p class="text-gray-700 dark:text-gray-300 mb-3">
                  Upgrading the web interface is straightforward: simply overwrite the webui files.
                </p>
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 border border-green-300 dark:border-gray-600">
                  <p class="text-sm text-gray-700 dark:text-gray-300">
                    <strong class="text-green-700 dark:text-green-400">✓ Your local configurations in</strong> <code class="bg-gray-200 dark:bg-gray-700 text-gray-800 dark:text-gray-200 px-2 py-1 rounded text-sm font-mono">config-site.php</code> remain untouched and will be preserved.
                  </p>
                </div>
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
            <a href="https://github.com/jsuto/piler/releases" target="_blank" rel="noopener noreferrer" class="block bg-white dark:bg-gray-800 rounded-lg p-6 hover:shadow-md transition-shadow border border-gray-200 dark:border-gray-700">
              <div class="flex items-center mb-3">
                <svg class="h-6 w-6 text-primary-light dark:text-primary-dark mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21h10a2 2 0 002-2V9.414a1 1 0 00-.293-.707l-5.414-5.414A1 1 0 0012.586 3H7a2 2 0 00-2 2v14a2 2 0 002 2z" />
                </svg>
                <span class="font-semibold text-gray-900 dark:text-white">Release Notes</span>
              </div>
              <p class="text-sm text-gray-600 dark:text-gray-400">View changelogs & updates</p>
            </a>
          </div>
        </div>

      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Upgrade Instructions - Piler Documentation',
  meta: [
    { name: 'description', content: 'Complete guide to upgrading Piler email archiving system across all versions with exact step-by-step commands.' }
  ]
})
</script>
