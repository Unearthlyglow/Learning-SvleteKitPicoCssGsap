<script>
	import '@picocss/pico';
	import gsap from 'gsap';
	import { onMount } from 'svelte';
	let src1 = './src/public/assets/lening.jpg';
	let src2 = './src/public/assets/album1.png';
	// let src4 = './src/public/assets/
	// let src5 = './src/public/assets/
	//Optimizing Pixel 2

	onMount(() => {
		const tl = gsap.timeline();
		const duration = 1;

		tl.from('.box', {
			duration,
			opacity: 0
		}).from(
			'.box',
			{
				duration,
				xPercent: 100,
				rotation: -90,
				yPercent: 100,
				ease: 'bounce.out'
			},
			`-=${duration * 0.75}`
		);
	});
</script>

<div class="container-fluid margo">
	<!-- <div class="box"><button>Eat it</button></div> -->

	<div class="block1"><img src={src1} alt="Thanks" /></div>
	<div class="block2">
		<iframe
			class="heaven"
			width="560"
			height="315"
			src="https://www.youtube.com/embed/vpcFWQ0LuVg"
			title="YouTube video player"
			frameborder="0"
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
			allowfullscreen
		/>
	</div>
	<div class="block3Container">
		<div class="album1--class"><img class="pizza" src={src2} alt="" /></div>
		<p class="outNow">Out Now</p>
		<p class="newAlbum">New Album, ‘Santa Rosa’ out now!</p>
		<a href="https://josielockhart.bandcamp.com/" role="button" class="contrast button1"
			>Music & Merch</a
		>
		<div class="spotify-album">
			<iframe
				style="border-radius:12px"
				src="https://open.spotify.com/embed/album/316Brk4Xo0Hmemx2U91IxM?utm_source=generator"
				title="home"
				width="100%"
				height="380"
				frameBorder="0"
				allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
				loading="lazy"
			/>
		</div>
	</div>
	<div class="block4" />
	<div class="block5" />
	<div class="block6" />
	<div class="block7" />
	<div class="block8" />
	<div class="block9" />
	<div class="block10" />
</div>

<style lang="scss">
	//Colors
	$base-color: #c6538c;

	//Grid Container
	.margo {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(30em, 1fr));
		// grid-template-rows: repeat(8, minmax(min-content, 20rem));
	}

	//Grid Items
	.block1 {
		grid-column: 1 / -1;
	}

	.block2 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/orangeBlock.jpg');
		background-size: cover;
		display: flex;
		justify-content: center;
	}

	.heaven {
		width: 40rem;
		height: 30rem;
		align-self: center;
		justify-self: center;
	}

	.block3Container {
		grid-column: 1 / -1;
		background-image: url('../public/assets/pinkBlock.jpg');
		background-size: cover;
		display: grid;
		grid-template-columns: 2, 1fr;
	}

	//Josie Lockhart Album Cover
	.album1--class {
		margin-top: 3rem;
		margin-left: 3rem;
		grid-column: 1;
		grid-row: 1;
	}

	.outNow {
		font-size: 2rem;
		font-weight: bold;
		grid-column: 2;
		grid-row: 1;
		text-align: center;
		align-self: center;
	}

	.newAlbum {
		font-size: 3rem;
		margin-top: 9rem;
		font-weight: bold;
		grid-column: 2;
		grid-row: 1;
		text-align: center;
		align-self: center;
	}

	.button1 {
		font-weight: bold;
		grid-column: 2;
		width: 50%;
		text-align: center;
		justify-self: center;
		transform: translateY(-7rem);
	}

	.spotify-album {
		margin-top: 5rem;
		margin-bottom: 3rem;
		grid-column: 1 / 3;
	}

	.block4 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/orangeBlock.jpg');
		background-size: cover;
	}

	.block5 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/pinkBlock.jpg');
		background-size: cover;
	}

	.block6 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/orangeBlock.jpg');
		background-size: cover;
	}

	.block7 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/pinkBlock.jpg');
		background-size: cover;
	}

	.block8 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/orangeBlock.jpg');
		background-size: cover;
	}

	.block9 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/pinkBlock.jpg');
		background-size: cover;
	}

	.block10 {
		grid-column: 1 / -1;
		height: 50rem;
		background-image: url('../public/assets/orangeBlock.jpg');
		background-size: cover;
	}

	// .box {
	// 	width: 100px;
	// 	height: 100px;
	//   background: $base-color;
	//   margin-bottom: 3rem;
	// }
</style>
