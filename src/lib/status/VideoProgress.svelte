<script lang="ts">
	import { linear } from 'svelte/easing';
	import { tweened } from 'svelte/motion';

	export let value = 0;
	export let duration = 1000 * (60 + 40); // 1 minute and 40 seconds

	const width$ = tweened(value, {
		easing: linear,
		duration(from, to) {
			const diff = Math.abs(to - from);

			return diff * duration;
		}
	});

	$: width$.set(value);
</script>

<div
	class="bg-gradient w-56 h-56 flex items-end justify-center rounded-2xl mb-10 overflow-hidden bg-neutral-200 dark:bg-neutral-800"
>
	<div
		class="w-full h-full flex flex-col items-center justify-center text- dark:text-white z-[1] relative"
	>
		<div
			class="progress-bar absolute left-0 top-0 h-full bg-[#627EEA] z-[-1]"
			style:width="{$width$ * 100}%"
		/>

		<div class="text-5xl font-bold max-w-full">{($width$ * 100).toFixed()} <span>%</span></div>

		<div class="text-lg font-medium opacity-50">complete</div>
	</div>
</div>

<style lang="postcss">
	.bg-gradient {
		@apply relative;
	}
</style>
