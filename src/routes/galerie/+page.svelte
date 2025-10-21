<script lang="ts">
	// IDs 1..10 – Dateiendungen brauchst du NICHT angeben
	const ids = Array.from({ length: 10 }, (_, i) => String(i + 1));

	type Pic = { id: string; alt: string };
	const images: Pic[] = ids.map((id, i) => ({
		id,
		alt:
			[
				'Nude Maniküre mit sanftem Glanz',
				'French Nails, klassisch',
				'Rosenholz-Farbton, kurz',
				'Soft Pink Gelmodellage',
				'Shellac Rot, hochglänzend',
				'Marmor-Design, subtil',
				'Milky Nails, natürlich',
				'Dezentes Glitzer-Highlight',
				'Ovalform, French modern',
				'Sommer-Design, Pastell'
			][i] ?? `Bild ${id}`
	}));

	let open = false;
	let idx = 0;
	const openAt = (i: number) => {
		idx = i;
		open = true;
	};
	const close = () => (open = false);
	const prev = () => (idx = (idx - 1 + images.length) % images.length);
	const next = () => (idx = (idx + 1) % images.length);
</script>

<section class="mx-auto max-w-6xl px-4 py-10" aria-label="Galerie">
	<h1 class="mb-6 font-[Fraunces] text-3xl">Galerie</h1>

	<div class="grid grid-cols-2 gap-3 md:grid-cols-3 lg:grid-cols-4">
		{#each images as img, i}
			<button
				class="group relative block aspect-square overflow-hidden rounded-2xl bg-[#e7e2e2] focus:outline-none focus-visible:ring-2 focus-visible:ring-[#b98b58]/50"
				on:click={() => openAt(i)}
				aria-label={`Bild vergrößern: ${img.alt}`}
			>
				<!-- Erst WebP versuchen, sonst PNG laden -->
				<picture>
					<source srcset={`/nails/galerie/${img.id}.webp`} type="image/webp" />
					<img
						src={`/nails/galerie/${img.id}.png`}
						alt={img.alt}
						class="h-full w-full object-cover transition-transform duration-300 group-hover:scale-[1.03]"
						loading="lazy"
						decoding="async"
						sizes="(max-width: 768px) 50vw, (max-width: 1024px) 33vw, 25vw"
					/>
				</picture>

				<div
					class="pointer-events-none absolute inset-0 bg-black/0 transition-colors group-hover:bg-black/10"
				></div>
			</button>
		{/each}
	</div>
</section>
