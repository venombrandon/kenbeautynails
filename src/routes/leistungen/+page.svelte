<script lang="ts">
	type Service = { name: string; price: string; note?: string };

	// --- Daten ---
	const mani: Service[] = [
		{ name: 'OPI Maniküre – mit Klarlack', price: '12€' },
		{ name: 'OPI Maniküre – mit Farblack', price: '20€' },
		{ name: 'OPI Maniküre – mit Shellac', price: '27€' }
	];

	const pedi: Service[] = [
		{ name: 'OPI Pediküre – mit Klarlack', price: '25€' },
		{ name: 'OPI Pediküre – mit Farblack', price: '30€' },
		{ name: 'OPI Pediküre – mit Shellac', price: '45€' },
		{ name: 'Shellac (nur Anwendung)', price: '25€', note: 'ohne Pediküre' }
	];

	const modellage: Service[] = [
		{ name: 'Neumodellage / Auffüllen – UV Gel-System', price: '37€', note: 'Natur oder French' },
		{ name: 'Neumodellage / Auffüllen – Pulver-System', price: '32€', note: 'Natur oder French' },
		{ name: 'Neumodellage / Auffüllen – Einfarbig / Verlauf', price: '37€' }
	];

	const design: Service[] = [
		{ name: 'Lackieren / Glitzer', price: '5€' },
		{ name: 'Extra lang', price: '5€' },
		{ name: 'Nailart – pro Finger', price: 'ab 1,50€' },
		{ name: 'Nailart – komplett', price: 'ab 10€' },
		{ name: 'Piercing', price: '5€' },
		{ name: 'Stein', price: 'ab 0,50€' },
		{ name: 'Kürzen, Feilen & Lackieren', price: '15€' },
		{ name: 'Reparatur', price: 'ab 3€' },
		{ name: 'Ablösen', price: '15€' }
	];

	const lashes: Service[] = [
		{ name: 'Wimpernverlängerung (1D–5D)', price: '60€' },
		{ name: 'Wimpern Auffüllen', price: 'ab 35€' }
	];

	function Category(title: string, items: Service[], subtitle?: string) {
		return `
      <div class="rounded-3xl border border-black/5 bg-white/80 backdrop-blur">
        <div class="px-6 py-4 border-b border-black/5 flex items-center justify-between">
          <div>
            <h2 class='font-[Fraunces] text-2xl'>${title}</h2>
            ${subtitle ? `<p class='text-sm text-[#3a3a3a]/70'>${subtitle}</p>` : ''}
          </div>
        </div>
        <ul class='divide-y divide-black/5'>
          ${items
						.map(
							(it) => `
            <li class='flex items-center justify-between px-6 py-3 hover:bg-[#e7e2e2]/30 transition-colors'>
              <div>
                <span class='font-medium'>${it.name}</span>
                ${it.note ? `<p class='text-sm text-[#3a3a3a]/70'>${it.note}</p>` : ''}
              </div>
              <div class='font-[Fraunces] text-lg text-[#b98b58]'>${it.price}</div>
            </li>`
						)
						.join('')}
        </ul>
      </div>
    `;
	}
</script>

<svelte:head>
	<title>Leistungen & Preise | KEN Beauty Nails</title>
	<meta
		name="description"
		content="Alle Leistungen & Preise von KEN Beauty Nails – Maniküre, Pediküre, Modellage, Naildesign & Wimpernverlängerung."
	/>
</svelte:head>

<section class="mx-auto max-w-6xl px-4 py-12">
	<h1 class="mb-2 text-center font-[Fraunces] text-4xl">Leistungen & Preise</h1>
	<p class="mb-10 text-center text-[#3a3a3a]/70">
		Ehrliche Preise. Hochwertige Produkte. Liebe zum Detail.
	</p>

	<div class="space-y-12">
		{@html Category('OPI Maniküre', mani)}
		{@html Category('OPI Pediküre', pedi)}
		{@html Category('Neumodellage & Auffüllen', modellage, '(Natur oder French)')}
		{@html Category('Design', design, 'Extras & Add-ons')}
		{@html Category('Wimpernverlängerung', lashes)}
	</div>

	<div class="mt-16 flex justify-center">
		<a
			href="https://kenbeautynails.setmore.com/book?step=time-slot&products=88c9fb65-6b34-4088-a936-50251fdc0400&type=service&staff=73b10dfb-56bd-4554-8e90-df71e12631b9&staffSelected=true"
			target="_blank"
			class="inline-flex items-center rounded-full bg-[#b98b58] px-6 py-3 font-medium text-white shadow-sm transition-colors hover:bg-[#a17b4d]"
		>
			Termin online buchen
		</a>
	</div>
</section>
