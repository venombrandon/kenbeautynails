<script lang="ts">
	// Optional: statisch ausliefern
	export const prerender = true;
</script>

<svelte:head>
	<title>Datenschutz | KEN Beauty Nails</title>
	<meta
		name="description"
		content="Datenschutzhinweise von KEN Beauty Nails gemäß DSGVO: Zwecke, Rechtsgrundlagen, Speicherdauer und Ihre Rechte."
	/>
</svelte:head>

<section class="mx-auto max-w-6xl px-4 py-12 leading-relaxed text-[#3a3a3a]">
	<div class="mx-auto max-w-3xl">
		<h1 class="mb-6 font-[Fraunces] text-3xl">Datenschutz</h1>
		<p class="text-sm text-[#3a3a3a]/70">Stand: {new Date().toLocaleDateString('de-DE')}</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">1. Verantwortlicher</h2>
		<p>
			<strong>KEN Beauty Nails</strong><br />
			Inhaberin: <strong>Vorname Nachname</strong><br />
			Stadtberg 37, 89312 Günzburg<br />
			Telefon:
			<a class="underline hover:text-[#b98b58]" href="tel:+4915203294243">0152 03294243</a><br />
			E-Mail:
			<a class="underline hover:text-[#b98b58]" href="mailto:tobavinh09@gmail.com"
				>tobavinh09@gmail.com</a
			>
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">2. Allgemeines zur Datenverarbeitung</h2>
		<p>
			Wir verarbeiten personenbezogene Daten ausschließlich im Rahmen der DSGVO. Je nach Nutzung
			unserer Website können folgende Datenarten betroffen sein: Bestandsdaten (z. B. Name,
			Kontakt), Inhaltsdaten (z. B. Nachrichten im Kontaktformular), Nutzungsdaten (z. B. besuchte
			Seiten, Zugriffszeiten), sowie Meta-/Kommunikationsdaten (z. B. IP-Adresse,
			Geräteinformationen).
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">3. Hosting & Server-Logs</h2>
		<p>
			Beim Aufruf unserer Seiten werden Server-Logfiles gespeichert (z. B. IP-Adresse in gekürzter
			Form, Zeitpunkt, abgerufene Datei, User-Agent). Die Verarbeitung erfolgt zur Sicherstellung
			des technischen Betriebs und der IT-Sicherheit (Art. 6 Abs. 1 lit. f DSGVO). Logdaten werden
			automatisiert in regelmäßigen Abständen gelöscht.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">4. Cookies & Einwilligungs-Management</h2>
		<p>
			Unsere Website kann Cookies nutzen. Notwendige Cookies sind zur Bereitstellung der Seite
			erforderlich (Art. 6 Abs. 1 lit. f DSGVO). Für optionale Dienste (z. B. eingebettete Inhalte)
			holen wir Einwilligungen über ein Einwilligungs-Banner ein (Art. 6 Abs. 1 lit. a DSGVO). Sie
			können Ihre Einwilligung jederzeit mit Wirkung für die Zukunft widerrufen.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">5. Online-Terminbuchung (Setmore)</h2>
		<p>
			Für die Online-Terminvergabe binden wir den Dienst <strong>Setmore</strong> ein. Bei Nutzung des
			Buchungs-Widgets werden Daten (z. B. Name, E-Mail, gewünschte Leistung, Terminzeit) an Setmore
			übertragen und dort verarbeitet. Rechtsgrundlage ist Ihre Einwilligung (Art. 6 Abs. 1 lit. a DSGVO)
			sowie die Durchführung vorvertraglicher Maßnahmen (Art. 6 Abs. 1 lit. b DSGVO). Wir laden das Widget
			erst nach Ihrem Klick („Buchungs-Widget laden“). Weitere Informationen finden Sie in den Datenschutzhinweisen
			von Setmore.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">6. Karten / Anfahrt (Google Maps, optional)</h2>
		<p>
			Sofern Sie eine eingebettete Karte aufrufen, werden Daten (z. B. IP-Adresse) an den Anbieter
			(Google) übertragen. Die Einbindung erfolgt nur nach Ihrer Einwilligung (Art. 6 Abs. 1 lit. a
			DSGVO). Alternativ stellen wir eine statische Karte oder einen externen Link bereit.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">7. Kontaktaufnahme</h2>
		<p>
			Bei der Kontaktaufnahme per E-Mail verarbeiten wir Ihre Angaben zur Bearbeitung der Anfrage
			(Art. 6 Abs. 1 lit. b DSGVO). Ihre Daten werden nach abschließender Bearbeitung bzw. gemäß
			gesetzlicher Aufbewahrungsfristen gelöscht.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">8. Social Media (z. B. Instagram, optional)</h2>
		<p>
			Verlinkungen auf Social-Media-Profile sind als externe Links gekennzeichnet. Beim Klick werden
			Daten an die jeweilige Plattform übertragen. Eine direkte Einbettung (Feed) erfolgt derzeit
			nicht ohne Ihre Einwilligung.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">9. Speicherdauer</h2>
		<p>
			Wir speichern personenbezogene Daten nur so lange, wie es für die jeweiligen Zwecke
			erforderlich ist oder wie es gesetzliche Aufbewahrungsfristen vorsehen. Danach werden die
			Daten gelöscht oder anonymisiert.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">10. Ihre Rechte</h2>
		<ul class="ml-5 list-disc space-y-1">
			<li>Auskunft über die verarbeiteten Daten (Art. 15 DSGVO)</li>
			<li>Berichtigung unrichtiger Daten (Art. 16 DSGVO)</li>
			<li>Löschung („Recht auf Vergessenwerden“, Art. 17 DSGVO)</li>
			<li>Einschränkung der Verarbeitung (Art. 18 DSGVO)</li>
			<li>Datenübertragbarkeit (Art. 20 DSGVO)</li>
			<li>Widerspruch gegen Verarbeitungen (Art. 21 DSGVO)</li>
			<li>Widerruf erteilter Einwilligungen (Art. 7 Abs. 3 DSGVO)</li>
		</ul>
		<p class="mt-3">
			Zudem haben Sie das Recht auf Beschwerde bei einer Aufsichtsbehörde, z. B. dem Bayerischen
			Landesamt für Datenschutzaufsicht.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">11. Auftragsverarbeitung / Empfänger</h2>
		<p>
			Wir setzen ggf. Dienstleister (z. B. Hosting, Buchung, E-Mail) im Rahmen von
			Auftragsverarbeitungsverträgen nach Art. 28 DSGVO ein. Eine Übermittlung in Drittländer findet
			nur statt, wenn geeignete Garantien vorliegen (z. B. EU-Standardvertragsklauseln).
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">12. Datensicherheit</h2>
		<p>
			Wir treffen technische und organisatorische Maßnahmen zur Sicherheit der Verarbeitung (z. B.
			TLS-Verschlüsselung, Zugriffsbeschränkungen) und passen diese regelmäßig an den Stand der
			Technik an.
		</p>

		<h2 class="mt-8 mb-3 font-[Fraunces] text-2xl">13. Änderungen dieser Hinweise</h2>
		<p>
			Wir passen diese Datenschutzhinweise an, wenn sich Funktionen, Rechtslagen oder Prozesse
			ändern. Bitte prüfen Sie diese Seite regelmäßig.
		</p>
	</div>
</section>
