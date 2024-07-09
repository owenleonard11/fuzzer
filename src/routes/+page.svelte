<script lang="ts">

	import '../app.postcss'
	import { TabGroup, TabAnchor, Modal } from '@skeletonlabs/skeleton'
	import { page } from '$app/stores';

	import { initializeStores } from '@skeletonlabs/skeleton';
	initializeStores();
	
</script>

<Modal />

<TabGroup class="text-3xl px-8 pt-8">
	<TabAnchor selected = {$page.url.pathname === "/"} href="/">
		<svelte:fragment slot="lead">Fuzzer</svelte:fragment>
	</TabAnchor>
	<TabAnchor selected = {$page.url.pathname === "/usage"} href="/usage">Usage</TabAnchor>
	<TabAnchor selected = {$page.url.pathname === "/about"} href="/about">About</TabAnchor>
</TabGroup>

<slot />
<div class="card text-xl p-4 mx-8">
	<code class="code">v0.1</code>
	<span>|</span> 
	<a href="https://github.com/owenleonard11/fuzzer" class="anchor">GitHub</a>
	<span>|</span>
	<a href="https://fuzzer.readthedocs.io/en/latest/" class="anchor">ReadTheDocs</a>
</div>