<script>
  import '@picocss/pico'
	import gsap from 'gsap';
	import { onMount } from 'svelte';
  

	onMount(() => {
		const tl = gsap.timeline();
		const duration = 1;
		
		tl.from('.box', {
			duration,
			opacity: 0
		})
		.from('.box', {
			duration,
			xPercent: 100,
			rotation: -90,
			yPercent: 100,
			ease: 'bounce.out',
		}, `-=${duration * 0.75}`)
	});
</script>

<div class="container-fluid">
<div class="box"><button>Eat it</button></div>
<p>SvelteKit</p>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus facilis officia impedit suscipit expedita, dolores veritatis odit esse quasi fugiat.</p>
<p>+</p>
<p>Pico CSS</p>
<p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Libero temporibus doloribus delectus ullam itaque quibusdam voluptatibus? Sapiente esse consequatur nemo iusto soluta neque quidem voluptas earum hic, assumenda labore at.</p>
<p>+</p>
<p>GSAP</p>
<p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptate laborum minima aut! Ipsam esse voluptatem itaque eos, deleniti culpa dolore. Quaerat dolore culpa ipsum, consequatur perferendis atque, ut aliquid minus voluptatibus similique maxime nobis est!</p>
</div>



<style>
	.box {
		width: 100px;
		height: 100px;
		background: rgb(123, 35, 35);
    margin-bottom: 3rem;
  
	}
</style>