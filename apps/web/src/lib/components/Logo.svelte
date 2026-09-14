<script lang="ts">
	interface Props {
		class?: string;
		width?: number;
		height?: number;
		showText?: boolean;
		decorative?: boolean;
	}

	let {
		class: className = '',
		width = 100,
		height = 28,
		showText = false,
		decorative = false
	}: Props = $props();
	const size = $derived(Math.min(width, height));
</script>

<div class="flex items-center gap-2 {className}">
	<span
		class="inline-block shrink-0"
		style="width:{size}px;height:{size}px;background-color:var(--action-focal);-webkit-mask-image:url('/assets/brand/mark.svg');mask-image:url('/assets/brand/mark.svg');-webkit-mask-size:contain;mask-size:contain;-webkit-mask-repeat:no-repeat;mask-repeat:no-repeat;"
		role={decorative || showText ? undefined : 'img'}
		aria-label={decorative || showText ? undefined : 'Blip Social'}
		aria-hidden={decorative || showText ? 'true' : undefined}
	></span>
	{#if showText}
		<span
			class="font-brand leading-none font-semibold tracking-[-0.02em] whitespace-nowrap text-sidebar-foreground"
			>Blip Social</span
		>
	{/if}
</div>
