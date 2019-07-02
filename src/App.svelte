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