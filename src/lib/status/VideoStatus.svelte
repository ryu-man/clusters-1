<script lang="ts">
</script>

<div class="flex flex-col items-center">
	<div class="bg-gradient w-56 h-56 flex items-end justify-center rounded-2xl mb-10">
		<div
			class="w-20 h-20 flex items-center justify-center rounded-full bg-blue-500 bg-opacity-5 border border-blue-500 border-opacity-90 z-10 translate-y-1/2"
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="47"
				height="48"
				viewBox="0 0 47 48"
				fill="none"
			>
				<path
					opacity="0.3"
					d="M23.5007 2C19.2401 2 15.0753 3.29028 11.5328 5.70767C7.99024 8.12506 5.22919 11.561 3.59876 15.581C1.96832 19.6009 1.54172 24.0244 2.37291 28.292C3.2041 32.5596 5.25575 36.4796 8.2684 39.5564C11.2811 42.6331 15.1194 44.7284 19.2981 45.5773C23.4768 46.4261 27.8081 45.9905 31.7443 44.3253C35.6805 42.6602 39.0449 39.8404 41.4119 36.2225C43.7789 32.6047 45.0423 28.3512 45.0423 24C45.0423 18.1652 42.7728 12.5695 38.7329 8.44365C34.6931 4.31785 29.2139 2 23.5007 2ZM23.5007 40C20.4021 40 17.3731 39.0616 14.7967 37.3035C12.2204 35.5454 10.2123 33.0466 9.02655 30.1229C7.84078 27.1993 7.53052 23.9823 8.13503 20.8786C8.73953 17.7749 10.2316 14.9239 12.4227 12.6863C14.6137 10.4487 17.4052 8.9248 20.4442 8.30744C23.4833 7.69007 26.6333 8.00693 29.496 9.21793C32.3587 10.4289 34.8055 12.4797 36.527 15.1109C38.2485 17.7421 39.1673 20.8355 39.1673 24C39.1673 28.2435 37.5167 32.3131 34.5787 35.3137C31.6406 38.3143 27.6557 40 23.5007 40Z"
					fill="#3B82F6"
				/>
				<path
					d="M19.8582 2.32C15.4778 3.07475 11.433 5.19411 8.27779 8.3878C5.12259 11.5815 3.01135 15.6933 2.23325 20.16C2.1398 20.5868 2.13356 21.0287 2.21491 21.4581C2.29627 21.8875 2.46348 22.2951 2.70609 22.6555C2.9487 23.0159 3.26149 23.3213 3.62492 23.5526C3.98834 23.784 4.39458 23.9363 4.81825 24C5.58098 24.0747 6.34253 23.846 6.9444 23.3618C7.54626 22.8775 7.94209 22.1748 8.0495 21.4C8.58329 18.0745 10.1316 15.006 12.4736 12.6321C14.8156 10.2582 17.8318 8.70008 21.092 8.18C21.7566 8.08837 22.3664 7.75453 22.809 7.24C23.2517 6.72547 23.4973 6.0649 23.5007 5.38C23.497 4.9207 23.3947 4.46783 23.201 4.05332C23.0072 3.63881 22.7268 3.27275 22.3795 2.98096C22.0321 2.68917 21.6263 2.47876 21.1907 2.36455C20.7551 2.25035 20.3002 2.23514 19.8582 2.32Z"
					fill="#3B82F6"
				>
					<animateTransform
						attributeName="transform"
						type="rotate"
						from="0 23.5 24"
						to="360 23.5 24"
						dur=".3s"
						repeatCount="indefinite"
					/>
				</path>
			</svg>
		</div>
	</div>

	<div class="mt-5" />

	<div class="flex flex-col items-center gap-2">
		<div class="text-[41.5px] font-bold text-center">Creating your video</div>
		<p class="opacity-50 font-medium text-center text-medium">
			We are creating a personalized .gif of <br /> your new Cluster, which you can <br /> share with
			your friends.
		</p>
	</div>
</div>

<style lang="postcss">
	.bg-gradient {
		@apply relative;
	}

	.bg-gradient:after {
		@apply absolute inset-0;

		content: '';
		background: linear-gradient(
			180deg,
			theme('colors.neutral.200') 0%,
			theme('colors.neutral.200') 28%,
			rgba(250, 250, 250, 0) 100%
		);
		border-radius: inherit;
	}

	@media (prefers-color-scheme: dark) {
		.bg-gradient:after {
			background: linear-gradient(
				180deg,
				theme('colors.neutral.700') 0%,
				theme('colors.neutral.700') 28%,
				rgba(255, 255, 255, 0) 100%
			);
		}
	}
</style>
