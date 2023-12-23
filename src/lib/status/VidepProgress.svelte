<script lang="ts">
	import { expoOut } from 'svelte/easing';
	import { tweened } from 'svelte/motion';

	export let value = 0;

	const width$ = tweened(value, { easing: expoOut });

	$: width$.set(value * 100, {
		duration(from, to) {
			const maxDuration = 1000 * 60 * 1.5; // 1:30 minutes
			const diff = Math.abs(to - from);

			return (diff / 100) * maxDuration;
		}
	});
</script>

<div
	class="bg-gradient w-56 h-56 flex items-end justify-center rounded-2xl mb-10 overflow-hidden bg-neutral-200 dark:bg-neutral-800"
>
	<div
		class="w-full h-full flex flex-col items-center justify-center text- dark:text-white z-[1] relative"
	>
		<div
			class="progress-bar absolute left-0 top-0 h-full bg-[#627EEA] z-[-1]"
			style:width="{$width$}%"
		/>

		<div class="text-5xl font-bold max-w-full">{$width$.toFixed()} <span>%</span></div>

		<div class="text-lg font-medium opacity-50">complete</div>
	</div>
</div>

<style lang="postcss">
	.bg-gradient {
		@apply relative;
	}
</style>
