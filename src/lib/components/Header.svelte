<script lang="ts">
	import { Menu, X, ChevronDown } from 'lucide-svelte';
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';

	let mobileOpen = false;
	let servicesOpen = false;

	let servicesRef: HTMLElement;

	const linkBase =
		'transition-colors duration-150 hover:text-[#b98b58] focus:outline-none focus-visible:ring-2 focus-visible:ring-[#b98b58]/50 rounded-sm uppercase';
</script>

<nav
	class="sticky top-0 z-50 bg-[#e7e2e2]/80 font-[Fraunces] shadow-[0_2px_6px_rgba(0,0,0,0.08)] backdrop-blur-md"
>
	<div class="mx-auto max-w-6xl px-4">
		<div class="flex items-center justify-between py-3">
			<a href="/" class="flex items-center">
				<img
					src="logo.png"
					alt="Logo"
					class="h-16 transition-transform duration-200 hover:scale-105 md:h-20"
				/>
			</a>

			<div class="hidden items-center gap-8 md:flex">
				<ul
					class="flex items-center gap-8 text-[1.05rem] font-semibold tracking-wide text-[#3a3a3a] uppercase"
				>
					<li><a href="/" class={linkBase}>Home</a></li>

					<li class="relative">
						<a href="/" class={linkBase}>Leistungen</a>
					</li>

					<li><a href="/galerie" class={linkBase}>Galerie</a></li>
					<li><a href="/kontakt" class={linkBase}>Kontakt</a></li>
				</ul>

				<a
					href="/buchen"
					class="inline-flex items-center rounded-full bg-[#b98b58] px-5 py-2 font-medium tracking-wide text-white shadow-sm transition-colors duration-200 hover:bg-[#a17b4d]"
				>
					Termin buchen
				</a>
			</div>

			<button
				class="inline-flex items-center justify-center rounded-md p-2 text-[#3a3a3a] hover:text-[#b98b58] focus:outline-none focus-visible:ring-2 focus-visible:ring-[#b98b58]/50 md:hidden"
				aria-label="Menü öffnen"
				aria-expanded={mobileOpen}
				on:click={() => (mobileOpen = !mobileOpen)}
			>
				{#if mobileOpen}<X size={24} />{:else}<Menu size={24} />{/if}
			</button>
		</div>
	</div>

	{#if mobileOpen}
		<div class="border-t border-black/5 md:hidden">
			<div
				class="space-y-2 bg-[#e7e2e2]/90 px-4 py-4 font-semibold tracking-wide text-[#3a3a3a] uppercase backdrop-blur"
			>
				<a href="/" class="block rounded-lg px-3 py-2 hover:text-[#b98b58]">Home</a>
				<a href="/ueber-uns" class="block rounded-lg px-3 py-2 hover:text-[#b98b58]">Über uns</a>

				<a href="/" class="block rounded-lg px-3 py-2 hover:text-[#b98b58]">Leistungen</a>

				<a href="/galerie" class="block rounded-lg px-3 py-2 hover:text-[#b98b58]">Galerie</a>
				<a href="/kontakt" class="block rounded-lg px-3 py-2 hover:text-[#b98b58]">Kontakt</a>

				<a
					href="/buchen"
					class="mt-2 inline-flex items-center rounded-full bg-[#b98b58] px-5 py-2 font-medium tracking-wide text-white shadow-sm transition-colors duration-200 hover:bg-[#a17b4d]"
				>
					Termin buchen
				</a>
			</div>
		</div>
	{/if}
</nav>

<style>
	.rotate-180 {
		transform: rotate(180deg);
		transition: transform 0.2s ease;
	}
</style>
