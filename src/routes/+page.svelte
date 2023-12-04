<script>
	import Contact from '$lib/components/Contact.svelte';
import Projects from '$lib/components/Projects.svelte';
	import Resume from '$lib/components/Resume.svelte';
	import { Avatar } from '@skeletonlabs/skeleton';
	import { filter, Rustic } from '@skeletonlabs/skeleton';
</script>

<hr class="!border-dotted my-5" />
<section class="flex justify-center items-center my-7 lg:mx-32 ">
	<div class="p-4 card shadow-2xl flex flex-col justify-between ">
		<div class="p-3">
			<div class="">
				<div class="flex items-center justify-center place-content-center my-2">
					<Avatar class=" shadow-2xl" src="https://avatars.githubusercontent.com/u/98795019?v=4" width="w-56" rounded="rounded-full" />
				</div>
			</div>
			<h1 class="h1 text-primary-500 mb-4 text-center">My name is Philip Rolfe</h1>
			
			<p class="lg:max-w-prose">
				I am a computer systems technology student with a passion for all things technological. I'm
				currently studying for an advanced diploma in this field and actively seeking out innovative
				& stimulating endeavours. I'm eager to further develop my skills as a tech-savvy
				professional, enthused to see where my talents might lead me in the long run.
			</p>
		</div>
		
		
		
	</div>
</section>
<hr class="!border-dotted my-5" />
<Projects />
<hr class="!border-dotted my-5" />
<Resume />
<hr class="!border-dotted my-5" />
<Contact />
<hr class="!border-dotted my-5" />
	<div class="fixed bottom-0 right-0 h-16 w-16 ...">
		<a href="#top">
			<div class="btn variant-filled-primary p-4">Top</div>
		</a>
	</div>


