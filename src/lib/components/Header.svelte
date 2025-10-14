<script lang="ts">
	import { Menu, X, ChevronDown } from 'lucide-svelte';
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';

	let mobileOpen = false;
	let servicesOpen = false;

	let servicesRef: HTMLElement;
	function onDocClick(e: MouseEvent) {
		if (servicesRef && !servicesRef.contains(e.target as Node)) servicesOpen = false;
	}
	onMount(() => {
		document.addEventListener('click', onDocClick);
		return () => document.removeEventListener('click', onDocClick);
	});

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

					<li class="relative" bind:this={servicesRef}>
						<button
							class={'flex cursor-pointer items-center gap-1 ' + linkBase}
							aria-haspopup="menu"
							aria-expanded={servicesOpen}
							on:click={() => (servicesOpen = !servicesOpen)}
						>
							Leistungen <ChevronDown size={18} />
						</button>

						{#if servicesOpen}
							<div
								in:fade={{ duration: 150 }}
								out:fade={{ duration: 100 }}
								role="menu"
								class="absolute left-0 mt-3 w-60 origin-top rounded-2xl border border-black/5
         bg-gradient-to-b from-white/90 to-[#e7e2e2]/90 p-1 shadow-[0_8px_30px_rgba(0,0,0,0.08)]
         ring-1 ring-black/5 backdrop-blur-md
         will-change-transform"
							>
								<span
									class="absolute -top-2 left-6 block h-4 w-4 rotate-45
               rounded-[6px] border border-black/5
               bg-white/90 backdrop-blur-md"
								></span>

								<nav class="flex flex-col gap-1 text-[#3a3a3a]">
									<a
										role="menuitem"
										href="/leistungen/haende"
										class="block rounded-xl px-4 py-2.5 text-[0.95rem] font-semibold tracking-wide
             transition-colors hover:bg-white/60 hover:text-[#b98b58]
             focus-visible:ring-2 focus-visible:ring-[#b98b58]/40 focus-visible:outline-none"
									>
										Hände
									</a>

									<a
										role="menuitem"
										href="/leistungen/fuesse"
										class="block rounded-xl px-4 py-2.5 text-[0.95rem] font-semibold tracking-wide
             transition-colors hover:bg-white/60 hover:text-[#b98b58]
             focus-visible:ring-2 focus-visible:ring-[#b98b58]/40 focus-visible:outline-none"
									>
										Füße
									</a>
								</nav>
							</div>
						{/if}
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

				<details class="group">
					<summary
						class="flex cursor-pointer list-none items-center justify-between rounded-lg px-3 py-2 hover:text-[#b98b58]"
					>
						<span>Leistungen</span>
						<ChevronDown size={18} class="transition-transform group-open:rotate-180" />
					</summary>
					<div class="mt-1 ml-3 space-y-1 font-medium normal-case">
						<a href="/leistungen/haende" class="block rounded-lg px-3 py-2 hover:bg-white/60"
							>Hände</a
						>
						<a href="/leistungen/fuesse" class="hover:bg白/60 block rounded-lg px-3 py-2">Füße</a>
					</div>
				</details>

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
