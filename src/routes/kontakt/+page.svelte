<script lang="ts">
	export const prerender = true;
	import { Phone, Mail, CalendarDays, MapPin } from 'lucide-svelte';
</script>

<svelte:head>
	<title>Kontakt | KEN Beauty Nails</title>
	<meta
		name="description"
		content="Kontaktiere KEN Beauty Nails in Günzburg – telefonisch, per E-Mail oder buche direkt online."
	/>
</svelte:head>

<section class="mx-auto max-w-6xl px-4 py-16 text-[#3a3a3a]">
	<header class="text-center">
		<h1 class="font-[Fraunces] text-3xl">Kontakt</h1>
		<p class="mt-2 text-[#3a3a3a]/80">Schnell & einfach – so erreichst du uns:</p>
	</header>

	<!-- 👇 Der Wrapper sorgt für vertikale Abstände zwischen seinen Kindern -->
	<div class="mt-8 space-y-12">
		<!-- Buttons -->
		<div class="grid gap-3 sm:grid-cols-3">
			<a
				href="tel:+4915203294243"
				class="group inline-flex items-center justify-center gap-2 rounded-full bg-[#b98b58] px-6 py-3 font-medium text-white shadow-sm transition-colors hover:bg-[#a17b4d]"
				aria-label="Jetzt anrufen"
			>
				<Phone size={18} class="shrink-0" />
				<span>Anrufen</span>
			</a>

			<!-- E-Mail -->
			<a
				href="mailto:tobavinh09@gmail.com"
				class="group inline-flex items-center justify-center gap-2 rounded-full border border-[#b98b58] px-6 py-3 font-medium text-[#b98b58] transition-colors hover:bg-[#b98b58]/10"
				aria-label="E-Mail schreiben"
			>
				<Mail size={18} class="shrink-0" />
				<span>E-Mail schreiben</span>
			</a>

			<!-- Termin buchen -->
			<a
				href="https://kenbeautynails.setmore.com/book?step=time-slot&products=13b7f265-ac5e-47fd-8bdd-96ea25d8a754&type=service&staff=e601a373-7f6d-4140-980c-ae947f3a19ad&staffSelected=true"
				target="_blank"
				class="group inline-flex items-center justify-center gap-2 rounded-full border border-black/10 bg-[#e7e2e2] px-6 py-3 font-medium transition-colors hover:bg-[#e7e2e2]/70"
				aria-label="Online Termin buchen"
			>
				<CalendarDays size={18} class="shrink-0" />
				<span>Termin buchen</span>
			</a>
		</div>

		<!-- Adresse & Öffnungszeiten -->
		<div
			class="grid gap-6 rounded-2xl border border-black/10 bg-white/90 p-6 backdrop-blur sm:grid-cols-2"
		>
			<div>
				<h2 class="mb-2 text-xl">Adresse</h2>
				<p class="flex items-start gap-2">
					<MapPin size={18} class="mt-0.5 shrink-0" />
					<span>Stadtberg 37<br />89312 Günzburg</span>
				</p>
			</div>

			<div>
				<h2 class="mb-2 text-xl">Öffnungszeiten</h2>
				<!-- eigenes Wrapper-Element sorgt dafür, dass mt- sicher greift -->
				<div class="space-y-1">
					<p>Mo–Fr: 10:00 – 19:00</p>
					<p>Sa: 10:00 – 17:30</p>
				</div>
			</div>
		</div>
	</div>
</section>
