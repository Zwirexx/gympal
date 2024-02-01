<script>
	import { ListBox, ListBoxItem } from '@skeletonlabs/skeleton';
	import { computePosition, autoUpdate, offset, shift, flip, arrow } from '@floating-ui/dom';
	import { popup } from '@skeletonlabs/skeleton';
	import { storePopup } from '@skeletonlabs/skeleton';

	storePopup.set({ computePosition, autoUpdate, offset, shift, flip, arrow });
	export let theme;

	const popupCombobox = {
		event: 'click',
		target: 'popupCombobox',
		placement: 'bottom',
		closeQuery: '.listbox-item'
	};
</script>

<button class="btn variant-ghost w-48 justify-between" use:popup={popupCombobox}>
	<span>Theme</span>
	<span>▼</span>
</button>

<div class="bg-surface-700 rounded-xl w-48 shadow-xl py-2" data-popup="popupCombobox">
	<ListBox rounded="rounded-none">
		<ListBoxItem bind:group={theme} name="medium" value="vintage">📺 Vintage</ListBoxItem>
		<ListBoxItem bind:group={theme} name="medium" value="crimson">🍎 Crimson</ListBoxItem>
		<ListBoxItem bind:group={theme} name="medium" value="wintry">❄️ Wintry</ListBoxItem>
		<ListBoxItem bind:group={theme} name="medium" value="gold-nouveau">✨ Gold Nouveau</ListBoxItem>
	</ListBox>
	<div class="arrow bg-surface-100-800-token" />
</div>
