<script>
	import '../app.css';
</script>

<br />
<hr class="h-px mx-8 bg-black border-0 dark:bg-gray-700" />
<hr class="h-px mx-8 bg-black border-0 dark:bg-gray-700" />
<div class="w-full flex justify-center text-center p-1">
	<a
		href="/"
		class="a bold mx-2 text-4xl transition-colors duration-300 text-[var(--pri)] hover:text-[var(--sec)]"
		>Divit</a
	>
	<div class="dropdown relative mx-2">
		<button
			class="a bold text-4xl transition-colors duration-300 hover:text-[var(--sec)] dropdown-btn"
			>Policy</button
		>
		<div class="dropdown-content absolute hidden text-[var(--sec)] pt-1">
			<a href="/Policy#asuc" class="a rounded-t py-2 px-4 block whitespace-no-wrap"
				>ASUC Reform</a
			>
			<a href="/Policy#campus" class="a py-2 px-4 block whitespace-no-wrap"
				>Campus Improvement</a
			>
			<a href="/Policy#mental" class="a py-2 px-4 block whitespace-no-wrap">Mental Health</a>
			<a href="/Policy#housing" class="a rounded-b py-2 px-4 block whitespace-no-wrap">Housing</a>
		</div>
	</div>
	<a
		href="/Endorsements"
		class="a bold mx-2 text-4xl transition-colors duration-300 hover:text-[var(--pri)]"
		>Endorsements</a
	>
	<a
		href="/Team"
		class="a bold mx-2 text-4xl transition-colors duration-300 hover:text-[var(--pri)]">Team</a
	>
</div>

<hr class="h-px mx-8 bg-black border-0 dark:bg-gray-700" />
<hr class="h-px mx-8 bg-black border-0 dark:bg-gray-700" />
<slot />

<style>
	:global(body) {
		letter-spacing: 0.1em;
	}

	/* Dynamic font size using viewport width (vw) */
	.a {
		font-size: 2.5vw; /* Adjust the vw value as needed */
	}

	/* Responsive font sizes for the navbar */
	@media (max-width: 1200px) {
		.a {
			font-size: 3vw; /* Increase the vw value as the screen gets smaller to maintain readability */
		}
	}

	@media (max-width: 768px) {
		.a {
			font-size: 4vw; /* Further increase the vw value for mobile screens */
		}
	}

	@media (max-width: 480px) {
		.a {
			font-size: 5.5vw; /* Even larger vw value for very small screens */
		}
	}

	/* Ensure font size doesn't get too small or too large */
	.a {
		font-size: clamp(1rem, 5vw, 3rem); /* Use clamp() to set a minimum and maximum font size */
	}

	.dropdown-btn:focus + .dropdown-content,
	.dropdown-btn:hover + .dropdown-content,
	.dropdown-content:hover {
		display: block;
	}

	.dropdown-content {
		display: none;
		position: absolute;
		background-color: var(--bg);
		min-width: 160px;
		box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
		z-index: 1;
	}

	.dropdown-content a {
		color: black;
		padding: 12px 16px;
		text-decoration: none;
		display: block;
	}

	.dropdown-content a:hover {
		background-color: var(--sec);
	}
</style>
