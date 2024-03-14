<script>
	import '../app.css';
	import sam from '$lib/sam_hero.png';
</script>

<div class="container">
	<div class="image-container">
		<img src={sam} alt="Sam Grotenstein" />
	</div>
	<div class="text-container my-3">
		<h1 class="text-center text-9xl text-[var(--pri)]">Divit Chopra</h1>
		<h3 class="text-center text-5xl text-[var(--sec)]">Divit for ASUC EVP</h3>
		<p class="text-center text-l my-3">
			Current systems block student-led initiatives; this must change. My campaign is committed to
			empowering student voices and driving progressive action. We're not just hoping for change,
			we're enacting it. Change is on the horizon, and with your support, it's inevitable.
		</p>
	</div>
</div>

<style lang="postcss">
	.container {
		display: flex;
		flex-direction: row; /* Default to row for larger screens */
		justify-content: center;
		align-items: center;
		height: 90vh; /* Use viewport height to make it take up full screen */
	}
	.image-container,
	.text-container {
		flex: 1; /* This will make both divs take up equal space */
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column; /* Stack children vertically */
		padding: 1rem;
	}
	img {
		max-width: 100%; /* Ensure the image is responsive and doesn't overflow */
		height: auto;
	}

	/* Responsive text sizes */
	h1 {
		font-size: 8rem; /* Adjust the size for mobile */
	}
	h3 {
		font-size: 4rem; /* Adjust the size for mobile */
	}
	p {
		font-size: 1rem; /* Adjust the size for mobile */
	}

	/* Media query for tablet and mobile screens */
	@media (max-width: 768px) {
		.container {
			flex-direction: column; /* Stack image-container and text-container */
			height: auto; /* Adjust height for smaller screens */
		}
		.image-container,
		.text-container {
			width: 90%; /* Full width containers for smaller screens */
		}
		/* Adjust text sizes for smaller screens */
		h1 {
			font-size: 4rem; /* Larger text size for smaller screens */
		}
		h3 {
			font-size: 2.5rem; /* Larger text size for smaller screens */
		}
		p {
			font-size: 1.25rem; /* Slightly larger text size for readability on smaller screens */
		}
	}
</style>
