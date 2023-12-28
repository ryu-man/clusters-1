<script lang="ts">
	import VidepProgress from './VideoProgress.svelte';

	export let progress = 0;
	export let duration = 1000 * (60 + 40); // 1 minute and 40 seconds
</script>

<div class="flex flex-col items-center">
	<VidepProgress value={progress} {duration} />

	<div class="mt-5" />

	<div class="flex flex-col items-center gap-2">
		<div class="text-3xl md:text-[41.5px] md:leading-[130%] font-bold text-center">
			Creating your video
		</div>
		<p class="opacity-50 font-medium text-center text-medium">
			We are creating a personalized .gif of <br /> your new Cluster, which you can <br /> share with
			your friends.
		</p>
	</div>
</div>
