<script lang="ts">
	import { CreatingStatus, VideoStatus, DoneStatus } from '$lib';
	import FadingCircles from '$lib/FadingCircles.svelte';

	let name = 'ryeshrimp';

	let status: 'creating' | 'video' | 'done' = 'video';

	let progress = 0.65;

	const url = 'clusters.xyz/ryeshrimp';

	function onShare() {
		navigator.clipboard.writeText(url);
	}
</script>

<div
	class="w-full h-full overflow-hidden flex flex-col items-center justify-center dark:bg-neutral-950"
>
	<!-- This is the component container -->
	<div class="flex flex-col px-7 w-full max-w-4xl text-black dark:text-white">
		<div class="mb-14">
			{#if status === 'creating'}
				<CreatingStatus {name} />
			{/if}
			{#if status === 'video'}
				<VideoStatus {progress} />
			{/if}
			{#if status === 'done'}
				<DoneStatus />
			{/if}
		</div>

		<div
			class="flex flex-col md:flex-row items-center md:justify-between gap-6 md:gap-16 text-black bg-neutral-100 border border-neutral-200 rounded-2xl py-5 px-6 md:px-8 relative dark:text-white dark:bg-neutral-900 dark:border-neutral-800"
		>
			<div class="flex flex-col">
				<h5 class="text-large-bold mb-1">Refer your friends</h5>
				<p class="opacity-50 font-medium">
					Earn money for inviting others to create their <br class="hidden xl:block" /> cluster, and
					prepare them for a multichain world
				</p>
			</div>

			<div
				class="flex flex-col md:flex-row gap-2.5 bg-opacity-0 bg-black md:bg-opacity-5 rounded-lg md:overflow-hidden h-fit min-w-fit relative z-10 backdrop-blur-xl w-full md:w-fit dark:bg-white dark:bg-opacity-0"
			>
				<div
					class="pl-4 py-2.5 whitespace-nowrap flex bg-black bg-opacity-5 rounded-lg md:rounded-r-none md:bg-opacity-0 dark:bg-white dark:bg-opacity-10"
				>
					<span class="opacity-50">https://</span>
					{url}
				</div>

				<button
					class="bg-black text-white font-medium p-2.5 rounded-lg min-w-min dark:bg-white dark:text-black"
					on:click={onShare}>Share</button
				>
			</div>

			<div class="absolute right-0 z-0 h-full">
				<FadingCircles />
			</div>
		</div>
	</div>
</div>
