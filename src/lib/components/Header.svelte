<script>
    import { getDrawerStore } from "@skeletonlabs/skeleton";

const drawerStore = getDrawerStore();

const drawerSettings = {
  id: 'example-3',
  meta: { foo: 'bar', fizz: 'buzz', age: 40 },
  // Provide your property overrides:
  bgDrawer: 'bg-surface-900 text-white',
  bgBackdrop: 'bg-gradient-to-tr from-surface-800/50 via-warning-500/50 to-pink-500/50',
  width: 'w-[280px] md:w-[480px]',
  padding: 'p-4',
  rounded: 'rounded-xl',
};

//drawerStore.open(drawerSettings);
function open(){
    drawerStore.open(drawerSettings);
}


</script>

<section class="flex justify-between mt-4 mx-2" >
    <h1 class="h1">
        <span class="bg-gradient-to-br from-red-500 to-yellow-500 bg-clip-text text-transparent box-decoration-clone">Philip </span>
        <span class="bg-gradient-to-br from-red-500 to-yellow-500 bg-clip-text text-transparent box-decoration-clone">Rolfe</span>
    </h1>
    <section class="hidden lg:flex justify-evenly gap-4">
        <a href="#projects"><h6 class="text-primary-400 hover:text-primary-300">Projects</h6></a>
        <a href="#gbc"><h6 class="text-primary-400 hover:text-primary-300">Education</h6></a>
        <a href="#certs"><h6 class="text-primary-400 hover:text-primary-300">Certifications</h6></a>
        <a href="#resume"><h6 class="text-primary-400 hover:text-primary-300">Resume</h6></a>
        <a href="#contact"><h6 class="text-primary-400 hover:text-primary-300">Contact</h6></a>
    </section>
    <button on:click={open} class=" lg:hidden btn variant-filled-primary ">Menu</button>
</section>

