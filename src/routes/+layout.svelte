<script>
	import '../app.postcss';
	import { AppShell, Drawer } from '@skeletonlabs/skeleton';
	import { autoModeWatcher } from '@skeletonlabs/skeleton';
    import { getDrawerStore } from "@skeletonlabs/skeleton";

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	import Header from '$lib/components/Header.svelte';
	import { initializeStores } from '@skeletonlabs/skeleton';
	initializeStores();

	const drawerStore = getDrawerStore();
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });

</script>
<Drawer >
    <section class="flex flex-col justify-center items-center gap-4 p-8">
        <a on:click={() => { drawerStore.close(); }} href="#projects"><h6 class=" h2 text-primary-400 hover:text-primary-300">Projects</h6></a>
        <a on:click={() => { drawerStore.close(); }} href="#gbc"><h6 class=" h2 text-primary-400 hover:text-primary-300">Education</h6></a>
        <a on:click={() => { drawerStore.close(); }} href="#certs"><h6 class=" h2 text-primary-400 hover:text-primary-300">Certifications</h6></a>
        <a on:click={() => { drawerStore.close(); }} href="#resume"><h6 class=" h2 text-primary-400 hover:text-primary-300">Resume</h6></a>
        <a on:click={() => { drawerStore.close(); }} href="#contact"><h6 class=" h2 text-primary-400 hover:text-primary-300">Contact</h6></a>
    </section>	
</Drawer>

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