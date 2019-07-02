
# svelte app issue

Based on https://github.com/sveltejs/template.

See version with issue here https://igtemplate.blob.core.windows.net/public/packages/svelte/public/index.html in Azure storage blob. Same code works in Svelte REPL

Just add this to App.svelte in Svelte REPL:

<script>
	import Loadable from 'svelte-loadable'
</script>

<h1>What now?</h1>
<Loadable  loader={() => import('https://igtemplate.blob.core.windows.net/public/packages/svelte/ScreenCDN.svelte')}>
  <div slot="loading">Loading...</div>
  <div slot="error" let:error>
    {error}
  </div>
</Loadable>
<mystuff/>	