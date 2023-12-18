<script lang="ts">
</script>

<div class="flex flex-col items-center">
	<div
		class="box w-56 h-56 bg-black rounded-2xl border-black border-opacity-10 border-2 dark:border-white dark:border-opacity-10"
	></div>

	<div class="mt-5" />

	<div class="flex flex-col items-center gap-2">
		<div class="text-3xl lg:text-[41.5px] font-bold text-center">Share with friends</div>
		<p class="opacity-50 font-medium text-center text-medium">
			Tell your friends about your new Cluster, <br /> and invite them to join.
		</p>
	</div>

	<div class="mt-7 flex flex-col lg:flex-row items-stretch justify-center gap-1.5 lg:gap-4">
		<div class="flex gap-4">
			<button
				class="bg-black text-white px-4 py-2.5 rounded-lg border border-[#404040] text-base flex items-center gap-2 dark:bg-white dark:text-black dark:border-neutral-700"
			>
				Download
			</button>

			<button
				class="px-4 py-2.5 rounded-lg border border-neutral-400 text-base flex items-center gap-2 dark:border-neutral-700"
			>
				Copy
			</button>
		</div>

		<div class="text-center relative w-full flex items-center gap-2">
			<div class="border-b border-black dark:border-white opacity-10 flex-1 lg:hidden" />

			<span class="opacity-50 text-mini lg:text-small leading-3">and</span>

			<div class="border-b border-black dark:border-white opacity-10 flex-1 lg:hidden" />
		</div>

		<button
			class="bg-[#1D9BF0] text-white px-4 py-2.5 rounded-lg border border-neutral-300 text-base flex items-center gap-2 dark:border-neutral-700"
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="21"
				height="16"
				viewBox="0 0 21 16"
				fill="none"
			>
				<path
					d="M18.8501 3.98316C18.8629 4.15675 18.8629 4.33034 18.8629 4.50553C18.8629 9.84359 14.5289 16 6.60414 16V15.9968C4.26313 16 1.97075 15.3712 0 14.1857C0.340402 14.2241 0.682511 14.2433 1.02547 14.2441C2.96551 14.2457 4.85009 13.6353 6.37636 12.5114C4.53272 12.4786 2.91603 11.3515 2.35125 9.706C2.99708 9.82279 3.66252 9.79879 4.2964 9.6364C2.28641 9.25563 0.840341 7.59973 0.840341 5.67665V5.62545C1.43924 5.93824 2.10981 6.11182 2.79573 6.13102C0.90262 4.9447 0.319074 2.58325 1.46228 0.736963C3.64973 3.2608 6.87715 4.79511 10.3417 4.9575C9.99452 3.55439 10.4689 2.08408 11.5882 1.09774C13.3235 -0.431763 16.0527 -0.353368 17.6839 1.27293C18.6488 1.09454 19.5736 0.762562 20.4199 0.292192C20.0982 1.22733 19.4251 2.02168 18.5259 2.52645C19.3799 2.43206 20.2143 2.21767 21 1.89049C20.4216 2.70324 19.693 3.41119 18.8501 3.98316Z"
					fill="white"
				/>
			</svg>

			<span>Share</span>
			<span class="lg:hidden">on Twitter</span>
		</button>
	</div>
</div>

<style>
	.box {
		box-shadow: 0px 4px 164px 0px rgba(0, 0, 0, 0.4);
	}

	@media (prefers-color-scheme: dark) {
		.box {
			box-shadow: 0px 4px 164px 0px rgba(255, 255, 255, 0.25);
		}
	}
</style>
