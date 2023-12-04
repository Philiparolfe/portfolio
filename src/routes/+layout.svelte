<script>
	import '../app.postcss';
	import { AppShell } from '@skeletonlabs/skeleton';
	import { autoModeWatcher } from '@skeletonlabs/skeleton';
	
	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	import Header from '$lib/components/Header.svelte';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>
<svelte:head>{@html `<script>${autoModeWatcher.toString()} autoModeWatcher();</script>`}</svelte:head>

<section class="mx-2 lg:mx-4  lg:p-4 ">
	<AppShell>
		<svelte:fragment slot="header">
			<Header />
			
		</svelte:fragment>
		<!-- (sidebarLeft) -->
		<!-- (sidebarRight) -->
		<!-- (pageHeader) -->
		<!-- Router Slot -->
		<slot />
		<!-- ---- / ---- -->
		<svelte:fragment slot="pageFooter">
			<div class="text-center">
				&copy; Copyright 2023, Philip Rolfe
			</div>
		</svelte:fragment>
		<!-- (footer) -->
	</AppShell>
</section>




<!--<slot />
-->