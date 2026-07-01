<script lang="ts">
	import { onMount } from 'svelte';

	const servicios = [
		{
			titulo: 'Administración de Redes',
			descripcion:
				'Configuración y mantenimiento de redes LAN/WAN, routers, switches y firewalls.',
			proyectos: 12,
			etiqueta: 'networking'
		},
		{
			titulo: 'Administración de Sistemas',
			descripcion:
				'Gestión de servidores Windows Server y Linux, Active Directory y políticas de grupo.',
			proyectos: 8,
			etiqueta: 'sysadmin'
		},
		{
			titulo: 'Infraestructura Cloud',
			descripcion:
				'Despliegue y gestión de servicios en la nube, virtualización y contenedores.',
			proyectos: 6,
			etiqueta: 'cloud'
		}
	];

	const estadisticas = [
		{ numero: '3', etiqueta: 'Años de estudio' },
		{ numero: '26', etiqueta: 'Proyectos completados' },
		{ numero: '99', etiqueta: 'Uptime %' }
	];

	const tecnologias = ['Linux', 'Docker', 'Redes', 'SSH', 'Minecraft Server'];

	let secciones = [
		{ id: 'servicios', label: 'Servicios' },
		{ id: 'proyectos', label: 'Proyectos' },
		{ id: 'educacion', label: 'Educación' },
		{ id: 'contacto', label: 'Contacto' }
	];

	onMount(() => {
		const observer = new IntersectionObserver(
			(entries) => {
				for (const entry of entries) {
					if (entry.isIntersecting) {
						entry.target.classList.add('is-visible');
						observer.unobserve(entry.target);
					}
				}
			},
			{ threshold: 0.15, rootMargin: '0px 0px -60px 0px' }
		);

		const revealEls = document.querySelectorAll('.reveal');
		revealEls.forEach((el) => observer.observe(el));

		return () => observer.disconnect();
	});
</script>

<svelte:head>
	<title>Joaquin Escudero — Analista en Infraestructura Informática</title>
	<meta
		name="description"
		content="Portfolio de Joaquin Escudero, estudiante de Analista en Infraestructura Informática en ORT Uruguay. Redes, sistemas y cloud."
	/>
</svelte:head>

{#snippet iconGithub()}
	<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"
		><path
			d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"
		/></svg
	>
{/snippet}

{#snippet iconArrow()}
	<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true"
		><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"
		/></svg
	>
{/snippet}

{#snippet iconExternal()}
	<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true"
		><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
		/></svg
	>
{/snippet}

{#snippet iconEmail()}
	<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true"
		><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
		/></svg
	>
{/snippet}

{#snippet iconNetwork()}
	<svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true"
		><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 4v6m0 4v6m-8-8h6m4 0h6M12 12m-3 0a3 3 0 106 0 3 3 0 10-6 0"
		/></svg
	>
{/snippet}

{#snippet iconServer()}
	<svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true"
		><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 7h14M5 12h14M5 17h14M7 7.01h.01M7 12.01h.01M7 17.01h.01"
		/></svg
	>
{/snippet}

{#snippet iconCloud()}
	<svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true"
		><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 15a4 4 0 004 4h10a4 4 0 002-7.5A5 5 0 008 9a4 4 0 00-5 6z"
		/></svg
	>
{/snippet}

<a
	href="#contenido"
	class="sr-only focus:not-sr-only focus:fixed focus:top-4 focus:left-4 focus:z-[100] focus:px-4 focus:py-2 focus:bg-primary focus:text-white focus:rounded-lg"
>
	Saltar al contenido
</a>

<header
	class="fixed top-0 left-0 right-0 z-50 bg-background/90 backdrop-blur-md border-b border-border"
>
	<nav class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between" aria-label="Navegación principal">
		<a href="/" class="font-display text-xl font-bold text-primary tracking-tight">JE.</a>
		<ul class="flex items-center gap-6 sm:gap-8">
			{#each secciones as seccion (seccion.id)}
				<li>
					<a
						href="#{seccion.id}"
						class="text-sm text-text-secondary hover:text-primary transition-colors"
					>
						{seccion.label}
					</a>
				</li>
			{/each}
		</ul>
	</nav>
</header>

<main id="contenido">
	<!-- Hero: terminal-inspired signature -->
	<section class="min-h-screen flex items-center pt-24 pb-16 px-6">
		<div class="max-w-6xl mx-auto w-full grid lg:grid-cols-[1.2fr_1fr] gap-12 items-center">
			<div class="space-y-8">
				<p class="font-mono text-sm text-accent tracking-wide">// estudiante de infraestructura</p>
				<div>
					<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold text-text-primary leading-[0.95] tracking-tight">
						Joaquin<br />Escudero
					</h1>
				</div>
				<p class="text-lg text-text-secondary max-w-md leading-relaxed">
					Analista en Infraestructura Informática, basado en Uruguay. Construyo y mantengo
					sistemas confiables — desde servidores hasta redes y cloud.
				</p>
				<div class="flex items-center gap-3">
					<a
						href="https://github.com/MatiasPriguetti03"
						target="_blank"
						rel="noopener noreferrer"
						aria-label="GitHub de Joaquin Escudero"
						class="w-11 h-11 rounded-lg bg-surface flex items-center justify-center text-text-secondary hover:bg-primary hover:text-white transition-colors"
					>
						{@render iconGithub()}
					</a>
				</div>
			</div>

			<!-- Signature: terminal panel -->
			<div class="reveal">
				<div class="bg-surface rounded-xl border border-border overflow-hidden shadow-2xl shadow-primary/10">
					<div class="flex items-center gap-2 px-4 py-3 border-b border-border bg-background/50">
						<span class="w-3 h-3 rounded-full bg-red-500/70"></span>
						<span class="w-3 h-3 rounded-full bg-yellow-500/70"></span>
						<span class="w-3 h-3 rounded-full bg-green-500/70"></span>
						<span class="ml-2 font-mono text-xs text-text-secondary">joaco@homelab: ~</span>
					</div>
					<div class="p-5 font-mono text-sm leading-relaxed space-y-2">
						<p class="text-text-secondary">$ <span class="text-accent">whoami</span></p>
						<p class="text-text-primary pl-4">joaquin_escudero</p>
						<p class="text-text-secondary">$ <span class="text-accent">cat</span> status.json</p>
						<p class="text-text-primary pl-4">{'{'}</p>
						<p class="pl-8 text-text-secondary">"<span class="text-primary">role</span>": <span class="text-text-primary">"infrastructure analyst"</span>,</p>
						<p class="pl-8 text-text-secondary">"<span class="text-primary">status</span>": <span class="text-green-400">"available"</span>,</p>
						<p class="pl-8 text-text-secondary">"<span class="text-primary">location</span>": <span class="text-text-primary">"Montevideo, UY"</span></p>
						<p class="text-text-primary pl-4">{'}'}</p>
						<p class="text-text-secondary">$ <span class="text-accent">uptime</span></p>
						<p class="text-text-primary pl-4">3 años estudiando · 26 labs completados</p>
						<p class="flex items-center gap-1 text-text-secondary">$ <span class="inline-block w-2 h-4 bg-accent animate-pulse"></span></p>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Servicios -->
	<section id="servicios" class="py-24 bg-surface/30 border-y border-border">
		<div class="max-w-6xl mx-auto px-6">
			<div class="reveal mb-14">
				<p class="font-mono text-sm text-accent mb-3">// especialidades</p>
				<h2 class="text-4xl lg:text-5xl font-bold text-text-primary tracking-tight">
					Servicios
				</h2>
			</div>
			<div class="grid md:grid-cols-3 gap-6">
				{#each servicios as servicio (servicio.etiqueta)}
					<article
						class="reveal bg-surface/50 rounded-xl p-7 border border-border hover:border-primary/50 transition-colors"
					>
						<div class="text-primary mb-5">
							{#if servicio.etiqueta === 'networking'}
								{@render iconNetwork()}
							{:else if servicio.etiqueta === 'sysadmin'}
								{@render iconServer()}
							{:else if servicio.etiqueta === 'cloud'}
								{@render iconCloud()}
							{/if}
						</div>
						<h3 class="text-xl font-semibold text-text-primary mb-3">{servicio.titulo}</h3>
						<p class="text-text-secondary text-sm leading-relaxed mb-6">{servicio.descripcion}</p>
						<div class="flex items-baseline gap-2 font-mono">
							<span class="text-3xl font-bold text-primary">{servicio.proyectos}</span>
							<span class="text-text-secondary text-xs">labs</span>
						</div>
					</article>
				{/each}
			</div>
		</div>
	</section>

	<!-- Sobre mí + Stats -->
	<section class="py-24 px-6">
		<div class="max-w-6xl mx-auto grid lg:grid-cols-2 gap-6">
			<div class="reveal bg-surface/40 rounded-xl p-8 border border-border">
				<h3 class="text-2xl font-semibold text-text-primary mb-4">Cualquier consulta o discusión</h3>
				<p class="text-text-secondary leading-relaxed mb-6">
					¿Tienes un proyecto en mente o quieres conversar sobre infraestructura informática?
					Estoy abierto a discutir oportunidades y formas de colaborar.
				</p>
				<a
					href="#contacto"
					class="inline-flex items-center gap-2 text-primary font-medium hover:text-accent transition-colors"
				>
					Hablemos
					{@render iconArrow()}
				</a>
			</div>
			<div class="reveal grid grid-cols-3 gap-4">
				{#each estadisticas as stat (stat.etiqueta)}
					<div class="bg-surface/40 rounded-xl p-6 border border-border flex flex-col justify-center text-center">
						<span class="font-mono text-4xl font-bold text-primary mb-1">{stat.numero}</span>
						<span class="text-text-secondary text-xs leading-tight">{stat.etiqueta}</span>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- Proyectos -->
	<section id="proyectos" class="py-24 bg-surface/30 border-y border-border">
		<div class="max-w-6xl mx-auto px-6">
			<div class="reveal mb-14">
				<p class="font-mono text-sm text-accent mb-3">// proyectos</p>
				<h2 class="text-4xl lg:text-5xl font-bold text-text-primary tracking-tight">
					Proyectos
				</h2>
			</div>
			<article class="reveal bg-surface/50 rounded-xl p-8 border border-border">
				<div class="flex flex-col lg:flex-row gap-8">
					<div class="lg:w-2/5">
						<div class="bg-background rounded-lg p-8 flex items-center justify-center aspect-video lg:aspect-square">
							<svg class="w-16 h-16 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 7h14M5 12h14M5 17h14M7 7.01h.01M7 12.01h.01M7 17.01h.01" />
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M14 7l3 3m0 0l-3 3m3-3h-7" class="text-accent" />
							</svg>
						</div>
					</div>
					<div class="lg:w-3/5">
						<p class="font-mono text-xs text-accent mb-2">// homelab</p>
						<h3 class="text-2xl font-semibold text-text-primary mb-3">Servidor Doméstico para Juegos</h3>
						<p class="text-text-secondary leading-relaxed mb-5">
							Construcción y operación de un servidor doméstico para alojar servidores de juegos
							como Minecraft y Counter-Strike. Incluye configuración de red, seguridad,
							mantenimiento y gestión de usuarios.
						</p>
						<ul class="flex flex-wrap gap-2 mb-6">
							{#each tecnologias as tech (tech)}
								<li class="px-3 py-1 bg-primary/10 text-primary rounded font-mono text-xs">{tech}</li>
							{/each}
						</ul>
						<a
							href="https://github.com/MatiasPriguetti03"
							target="_blank"
							rel="noopener noreferrer"
							class="inline-flex items-center gap-2 text-primary font-medium hover:text-accent transition-colors"
						>
							Ver en GitHub
							{@render iconExternal()}
						</a>
					</div>
				</div>
			</article>
		</div>
	</section>

	<!-- Educación -->
	<section id="educacion" class="py-24 px-6">
		<div class="max-w-4xl mx-auto">
			<div class="reveal mb-14">
				<p class="font-mono text-sm text-accent mb-3">// formación</p>
				<h2 class="text-4xl lg:text-5xl font-bold text-text-primary tracking-tight">
					Educación
				</h2>
			</div>
			<div class="reveal bg-surface/50 rounded-xl p-8 border border-border">
				<div class="flex items-start gap-6">
					<div class="w-14 h-14 rounded-lg bg-primary/15 flex items-center justify-center flex-shrink-0 text-primary">
						<svg class="w-7 h-7" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 14l9-5-9-5-9 5 9 5z M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z M12 14l-9 5 9 5 9-5-9-5z" />
						</svg>
					</div>
					<div class="flex-1">
						<h3 class="text-2xl font-semibold text-text-primary mb-1">
							Analista en Infraestructura Informática
						</h3>
						<p class="text-accent font-mono text-sm mb-4">ORT Uruguay</p>
						<p class="text-text-secondary leading-relaxed mb-6">
							Carrera técnica enfocada en administración de sistemas, redes de computadoras,
							infraestructura cloud, virtualización y seguridad informática.
						</p>
						<div class="grid sm:grid-cols-3 gap-4">
							{#each estadisticas as stat (stat.etiqueta)}
								<div class="bg-background/60 rounded-lg p-4 text-center">
									<span class="font-mono text-2xl font-bold text-primary block">{stat.numero}</span>
									<span class="text-text-secondary text-xs">{stat.etiqueta}</span>
								</div>
							{/each}
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Contacto -->
	<section id="contacto" class="py-24 bg-surface/30 border-t border-border">
		<div class="max-w-2xl mx-auto px-6">
			<div class="reveal mb-14 text-center">
				<p class="font-mono text-sm text-accent mb-3">// contacto</p>
				<h2 class="text-4xl lg:text-5xl font-bold text-text-primary tracking-tight">
					Hablemos
				</h2>
			</div>
			<div class="reveal bg-surface/50 rounded-xl p-6 border border-border">
				<div class="space-y-4">
					<a
						href="mailto:joaquin.escudero@email.com"
						class="flex items-center gap-4 p-4 bg-background/60 rounded-lg hover:bg-primary/10 transition-colors group"
					>
						<div class="w-12 h-12 rounded-lg bg-primary/15 flex items-center justify-center text-primary group-hover:bg-primary/25 transition-colors">
							{@render iconEmail()}
						</div>
						<div>
							<p class="font-mono text-xs text-text-secondary">Email</p>
							<p class="text-text-primary font-medium">joaquin.escudero@email.com</p>
						</div>
					</a>
					<a
						href="https://github.com/MatiasPriguetti03"
						target="_blank"
						rel="noopener noreferrer"
						class="flex items-center gap-4 p-4 bg-background/60 rounded-lg hover:bg-primary/10 transition-colors group"
					>
						<div class="w-12 h-12 rounded-lg bg-primary/15 flex items-center justify-center text-primary group-hover:bg-primary/25 transition-colors">
							{@render iconGithub()}
						</div>
						<div>
							<p class="font-mono text-xs text-text-secondary">GitHub</p>
							<p class="text-text-primary font-medium">@MatiasPriguetti03</p>
						</div>
					</a>
				</div>
			</div>
		</div>
	</section>
</main>

<footer class="py-8 border-t border-border">
	<div class="max-w-6xl mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-4">
		<p class="font-mono text-sm text-text-secondary">
			© 2025 Joaquin Escudero
		</p>
		<p class="font-mono text-xs text-text-secondary">
			Hecho con Svelte + Tailwind
		</p>
	</div>
</footer>
