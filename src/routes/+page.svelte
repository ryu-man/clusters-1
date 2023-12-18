<script lang="ts">
	import { CreatingStatus, VideoStatus, DoneStatus } from '$lib';
	import FadingCircles from '$lib/FadingCircles.svelte';

	let name = 'ryeshrimp';

	let status: 'creating' | 'video' | 'done' = 'creating';

	const url = 'clusters.xyz/ryeshrimp';

	const components: Record<
		string,
		{ component: ConstructorOfATypedSvelteComponent; props: Record<string, any> }
	> = {
		creating: {
			component: CreatingStatus,
			props: {
				name
			}
		},
		video: {
			component: VideoStatus,
			props: {}
		},
		done: {
			component: DoneStatus,
			props: {}
		}
	};

	function onShare() {
		navigator.clipboard.writeText(url);
	}
</script>

<div
	class="w-full h-full overflow-hidden flex flex-col items-center justify-center dark:bg-neutral-950"
>
	<!-- This is the component container -->
	<div class="flex flex-col px-32 text-black dark:text-white">
		<div class="mb-14">
			<svelte:component this={components[status].component} {...components[status].props} />
		</div>

		<div
			class="flex items-center gap-20 text-black bg-neutral-100 border border-neutral-200 rounded-2xl py-5 px-8 relative dark:text-white dark:bg-neutral-900 dark:border-neutral-800"
		>
			<div class="flex flex-col">
				<h5 class="text-large-bold mb-1">Refer your friends</h5>
				<p class="opacity-50 font-medium">
					Earn money for inviting others to create their <br class="hidden xl:block" /> cluster, and
					prepare them for a multichain world
				</p>
			</div>

			<div
				class="flex bg-black bg-opacity-5 rounded-lg overflow-hidden h-fit min-w-fit relative z-10 backdrop-blur-xl dark:bg-white dark:bg-opacity-10"
			>
				<div class="px-4 py-2.5 whitespace-nowrap flex">
					<span class="opacity-50">https://</span>
					{url}
				</div>

				<button
					class="bg-black text-white font-medium p-2.5 rounded-lg min-w-min dark:bg-white dark:text-black"
					on:click={onShare}>Share</button
				>
			</div>

			<div class="absolute right-0 z-0">
				<FadingCircles />
			</div>
		</div>
	</div>
</div>
