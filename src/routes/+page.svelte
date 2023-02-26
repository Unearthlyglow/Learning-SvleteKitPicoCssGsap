<script>
	import '@picocss/pico';
	import gsap from 'gsap';
	import { onMount } from 'svelte';
	import picture from '../public/assets/globe.png';
	let src1 = './src/public/assets/lening.jpg';
	let src2 = './src/public/assets/album1.png';
	let src3 = './src/public/assets/cold.png';
	let globe = './src/public/assets/globe.png';

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

	<div class="block1">
		<img class="globe" src={picture} alt="" />
		<div class="socialsHeader">
			<p>Social Social Social Social Social</p>
		</div>
	</div>
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
	<div class="block3">
		<div class="album1--class"><img src={src2} alt="" /></div>

		<div class="santaRosa">
			<p class="newAlbum">New Album, ‘Santa Rosa’ out now!</p>
			<a href="https://josielockhart.bandcamp.com/" role="button" class="contrast button1"
				>Music & Merch</a
			>
		</div>
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
	<div class="block4">
		<div class="coldWrapper" />
		<div class="album2--class"><img src={src3} alt="Colder Than Ice Album Cover" /></div>
		<div class="cold">
			<p class="newAlbum2">New Single - Colder Than Ice</p>
			<div class="button2">
				<a href="https://josielockhart.bandcamp.com/" role="button" class="contrast btn2"
					>Listen Now</a
				>
			</div>
		</div>
	</div>
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
		height: 50rem;
		background-image: url('../public/assets/3.png');
		background-size: cover;
		background-position: center;
		display: flex;
		flex-direction: column;
		justify-content: start;

		.globe {
			height: 5rem;
			align-self: start;
		}

		.socialsHeader {
			display: flex;
			word-spacing: 0.5em;
			align-self: end;
			margin-right: 2rem;
			transform: translateY(-3rem);
		}
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

	.block3 {
		grid-column: 1 / -1;
		background-image: url('../public/assets/pinkBlock.jpg');
		background-size: cover;
		display: flex;
		flex-wrap: wrap;
		align-items: stretch;

		//Josie Lockhart Album Cover
		.album1--class {
			margin-top: 3rem;
			margin-left: 3rem;
		}
		.santaRosa {
			text-align: center;
			align-self: center;
		}

		.newAlbum {
			font-size: 3.2rem;
			font-weight: bold;
			margin: 3rem;
		}

		.button1 {
			font-weight: bold;
			width: 30%;
		}

		.spotify-album {
			margin-top: 5rem;
			margin-bottom: 3rem;
			flex-grow: 1;
		}
	}

	.block4 {
		grid-column: 1 / -1;
		background-image: url('../public/assets/orangeBlock.jpg');
		background-size: cover;
		display: flex;

		.album2--class {
			margin: 2rem;
		}

		.cold {
			text-align: center;
			align-self: center;
		}
		.newAlbum2 {
			font-size: 3rem;
			color: black;
			font-weight: bolder;
			margin: 1rem;
		}

		.btn2 {
			font-weight: bold;
			margin: 1rem;
			background-color: black;
			color: white;
			border: 0;
		}
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
