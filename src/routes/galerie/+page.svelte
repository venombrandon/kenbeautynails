<script lang="ts">
	type Pic = { base: string; alt: string };
	const images: Pic[] = [
		{ base: '/nails/galerie/1', alt: 'Nude Maniküre mit sanftem Glanz' },
		{ base: '/nails/galerie/2', alt: 'French Nails, klassisch' },
		{ base: '/nails/galerie/3', alt: 'Rosenholz-Farbton, kurz' },
		{ base: '/nails/galerie/4', alt: 'Soft Pink Gelmodellage' },
		{ base: '/nails/galerie/5', alt: 'Shellac Rot, hochglänzend' },
		{ base: '/nails/galerie/6', alt: 'Marmor-Design, subtil' },
		{ base: '/nails/galerie/7', alt: 'Milky Nails, natürlich' },
		{ base: '/nails/galerie/8', alt: 'Dezentes Glitzer-Highlight' },
		{ base: '/nails/galerie/9', alt: 'Ovalform, French modern' },
		{ base: '/nails/galerie/10', alt: 'Ovalform, French modern' }
	];

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
				<img
					src={`${img.base}.webp`}
					alt={img.alt}
					class="h-full w-full object-cover transition-transform duration-300 group-hover:scale-[1.03]"
					loading="eager"
					sizes="(max-width: 768px) 50vw, (max-width: 1024px) 33vw, 25vw"
				/>
				<div
					class="pointer-events-none absolute inset-0 bg-black/0 transition-colors group-hover:bg-black/10"
				></div>
			</button>
		{/each}
	</div>
</section>
