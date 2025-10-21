<script lang="ts">
	import { Star, ArrowRight, Sparkles, ShieldCheck, Clock, MapPin } from 'lucide-svelte';

	const usp = [
		{ icon: ShieldCheck, title: 'Hygiene first', body: 'Sterile Instrumente & Einmalmaterial.' },
		{ icon: Sparkles, title: 'Top Produkte', body: 'Geprüfte Marken – lange Haltbarkeit.' },
		{ icon: Clock, title: 'Flexible Termine', body: 'Auch kurzfristig buchbar.' }
	];

	const rating = { value: 4.9, count: 128 };

	// Main SLogan: Schöne Nägel – stilvoll und präzise.
</script>

<svelte:head>
	<title>Elegante Nägel, entspannter Service | KEN Beauty Nails</title>
	<meta
		name="description"
		content="Nagelstudio in Günzburg: Maniküre, Gel, Shellac & Nail Art. Hochwertige Produkte, sterile Hygiene & flexible Termine. Jetzt Termin sichern."
	/>
	<meta property="og:title" content="KEN Beauty Nails – Nagelstudio in Günzburg" />
	<meta
		property="og:description"
		content="Schöne Nägel – stilvoll und präzise. Termine jetzt online buchen."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:image" content="/nails/main.png" />

	<script type="application/ld+json">
		{
			"@context": "https://schema.org",
			"@type": "NailSalon",
			"name": "KEN Beauty Nails",
			"image": "/nails/main.png",
			"address": {
				"@type": "PostalAddress",
				"streetAddress": "Stadtberg 37",
				"addressLocality": "Günzburg",
				"postalCode": "89312",
				"addressCountry": "DE"
			},
			"telephone": "08221 9668056",
			"url": "kenbeautynails.de",
			"priceRange": "€€",
			"aggregateRating": { "@type": "AggregateRating", "ratingValue": "4.9", "reviewCount": "128" },
			"openingHours": "Mo-Fr 09:00-19:00, Sa 09:00-17:30"
		}
	</script>
</svelte:head>

<section class="relative isolate mt-8 overflow-hidden rounded-3xl">
	<div
		class="pointer-events-none absolute inset-0 [mask-image:radial-gradient(70%_60%_at_50%_0%,black,transparent)]"
	></div>

	<div class="mx-auto grid max-w-6xl items-center gap-10 px-4 py-16 md:grid-cols-2">
		<div>
			<h1 class="font-[Fraunces] text-4xl leading-tight md:text-5xl">
				Elegante Nägel, <span class="text-[#b98b58]">entspannter Service</span>.
			</h1>
			<p class="mt-4 text-[#3a3a3a]/80">
				Maniküre, Gel, Shellac und Nail Art – präzise, sauber und schön.
			</p>

			<div class="mt-6 flex flex-wrap gap-3">
				<a
					href="https://kenbeautynails.setmore.com/book?step=time-slot&products=13b7f265-ac5e-47fd-8bdd-96ea25d8a754&type=service&staff=e601a373-7f6d-4140-980c-ae947f3a19ad&staffSelected=true"
					target="_blank"
					class="inline-flex items-center gap-2 rounded-full bg-[#b98b58] px-6 py-3 font-medium text-white shadow-sm transition-colors hover:bg-[#a17b4d]"
				>
					Termin sichern <ArrowRight size={18} />
				</a>
				<a
					href="/leistungen"
					class="inline-flex items-center gap-2 rounded-full border px-6 py-3 transition-colors hover:border-[#b98b58] hover:text-[#b98b58]"
				>
					Leistungen ansehen
				</a>
			</div>

			<div class="mt-6 flex items-center gap-3 text-sm text-[#3a3a3a]/80">
				<div class="flex items-center gap-1">
					{#each Array(5) as _}<Star size={16} class="fill-current" />{/each}
				</div>
				<span class="font-medium">{rating.value} / 5</span>
				<span>·</span>
				<span>{rating.count}+ Bewertungen</span>
			</div>
		</div>

		<div class="aspect-[4/3] overflow-hidden rounded-3xl bg-[#e7e2e2] shadow-lg">
			<img
				src="/nails/main.webp"
				alt="Nageldesign Close-up"
				class="h-full w-full object-cover"
				loading="lazy"
			/>
		</div>
	</div>
</section>

<section class="mx-auto max-w-6xl px-4 py-12">
	<div class="grid gap-6 md:grid-cols-3">
		{#each usp as u}
			<article
				class="rounded-2xl border border-black/5 bg-white/80 p-6 backdrop-blur transition-shadow hover:shadow-md"
			>
				<div class="flex items-center gap-3">
					<svelte:component this={u.icon} size={22} />
					<h3 class="font-semibold">{u.title}</h3>
				</div>
				<p class="mt-2 text-[#3a3a3a]/70">{u.body}</p>
			</article>
		{/each}
	</div>
</section>

<section class="mx-auto max-w-6xl px-4 py-12">
	<h2 class="mb-6 font-[Fraunces] text-3xl">Was Kund:innen sagen</h2>
	<div class="grid gap-6 md:grid-cols-3">
		{#each [1, 2, 3] as _}
			<figure class="rounded-2xl border border-black/5 bg-white/80 p-6 backdrop-blur">
				<div class="text-lg">★ ★ ★ ★ ★</div>
				<blockquote class="mt-2 text-[#3a3a3a]/80">
					„Super freundlich und sehr sauber gearbeitet. Absolute Empfehlung!“
				</blockquote>
				<figcaption class="mt-4 text-sm text-[#3a3a3a]/60">— Kundin A</figcaption>
			</figure>
		{/each}
	</div>
</section>

<section class="mx-auto max-w-6xl px-4 py-12">
	<div class="grid items-stretch gap-6 md:grid-cols-3">
		<div class="rounded-2xl border border-black/5 bg-white/80 p-6 backdrop-blur md:col-span-1">
			<h3 class="font-[Fraunces] text-2xl">Besuch uns</h3>
			<p class="mt-2 flex items-start gap-2 text-[#3a3a3a]/80">
				<MapPin size={18} class="mt-1" /> Stadtberg 37, 89312 Günzburg
			</p>
			<div class="mt-4 flex gap-3">
				<a
					href="/kontakt"
					class="rounded-full border px-4 py-2 transition-colors hover:border-[#b98b58] hover:text-[#b98b58]"
					>Kontakt</a
				>
				<a
					href="https://kenbeautynails.setmore.com/book?step=time-slot&products=13b7f265-ac5e-47fd-8bdd-96ea25d8a754&type=service&staff=e601a373-7f6d-4140-980c-ae947f3a19ad&staffSelected=true"
					target="_blank"
					class="rounded-full bg-[#b98b58] px-4 py-2 text-white transition-colors hover:bg-[#a17b4d]"
					>Termin buchen</a
				>
			</div>
		</div>
		<div class="overflow-hidden rounded-2xl border border-black/5 md:col-span-2">
			<iframe
				title="Anfahrt"
				src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d4496.295081886109!2d10.270072977493994!3d48.45469722902936!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x479945d9072f140d%3A0x69997ad95da15ceb!2sKEN%20Beauty%20Nails!5e1!3m2!1sde!2sde!4v1760448666603!5m2!1sde!2sde"
				class="h-[320px] w-full"
				loading="lazy"
				referrerpolicy="no-referrer-when-downgrade"
			></iframe>
		</div>
	</div>
</section>
