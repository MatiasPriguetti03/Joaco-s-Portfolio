<script lang="ts">
	const servicios = [
		{
			titulo: 'Administración de Redes',
			descripcion: 'Configuración y mantenimiento de redes LAN/WAN, routers, switches y firewalls.',
			proyectos: 12,
			icono: '🌐'
		},
		{
			titulo: 'Administración de Sistemas',
			descripcion: 'Gestión de servidores Windows Server y Linux, Active Directory y políticas de grupo.',
			proyectos: 8,
			icono: '🖥️'
		},
		{
			titulo: 'Infraestructura Cloud',
			descripcion: 'Despliegue y gestión de servicios en la nube, virtualización y contenedores.',
			proyectos: 6,
			icono: '☁️'
		}
	];

	const estadisticas = [
		{ numero: '3', etiqueta: 'Años de Estudio' },
		{ numero: '26', etiqueta: 'Proyectos Completados' }
	];

	const redesSociales = [
		{ nombre: 'GitHub', url: 'https://github.com/MatiasPriguetti03', icono: 'github' },
		{ nombre: 'LinkedIn', url: '#', icono: 'linkedin' }
	];
</script>

<svelte:head>
	<title>Joaquin Escudero | Analista en Infraestructura Informática</title>
	<meta name="description" content="Portfolio de Joaquin Escudero, estudiante de Analista en Infraestructura Informática en ORT Uruguay." />
</svelte:head>

<nav class="fixed top-0 left-0 right-0 z-50 bg-[#0a1628]/90 backdrop-blur-md border-b border-[#1e3a5f]">
	<div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
		<a href="/" class="text-xl font-bold text-[#3b82f6]">JE.</a>
		<div class="flex items-center gap-8">
			<a href="#servicios" class="text-[#94a3b8] hover:text-[#3b82f6] transition-colors">Servicios</a>
			<a href="#proyectos" class="text-[#94a3b8] hover:text-[#3b82f6] transition-colors">Proyectos</a>
			<a href="#educacion" class="text-[#94a3b8] hover:text-[#3b82f6] transition-colors">Educación</a>
			<a href="#contacto" class="px-4 py-2 bg-[#3b82f6] rounded-lg text-white font-medium hover:bg-[#2563eb] transition-colors">Contacto</a>
		</div>
	</div>
</nav>

<section class="min-h-screen flex items-center pt-20">
	<div class="max-w-7xl mx-auto px-6 py-20 grid lg:grid-cols-2 gap-12 items-center">
		<div class="space-y-8">
			<div>
				<p class="text-[#06b6d4] font-medium mb-2">Hola, soy</p>
				<h1 class="text-5xl lg:text-7xl font-extrabold text-white leading-tight">
					Joaquin<br />Escudero
				</h1>
			</div>
			<p class="text-xl text-[#94a3b8]">
				Analista en Infraestructura Informática, basado en Uruguay.
			</p>
			<div class="flex items-center gap-4">
				{#each redesSociales as red}
					<a
						href={red.url}
						target="_blank"
						rel="noopener noreferrer"
						class="w-10 h-10 rounded-full bg-[#1e3a5f] flex items-center justify-center text-[#94a3b8] hover:bg-[#3b82f6] hover:text-white transition-all"
					>
						{#if red.icono === 'github'}
							<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
						{:else if red.icono === 'linkedin'}
							<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
						{/if}
					</a>
				{/each}
			</div>
		</div>
		<div class="flex justify-center lg:justify-end">
			<div class="relative">
				<div class="absolute inset-0 bg-[#3b82f6]/20 rounded-full blur-3xl"></div>
				<div class="w-72 h-72 lg:w-96 lg:h-96 bg-gradient-to-br from-[#1e3a5f] to-[#0a1628] rounded-full flex items-center justify-center border-4 border-[#3b82f6]/30">
					<span class="text-8xl lg:text-9xl">👨‍💻</span>
				</div>
			</div>
		</div>
	</div>
</section>

<section id="servicios" class="py-20 bg-[#0f172a]">
	<div class="max-w-7xl mx-auto px-6">
		<div class="text-center mb-16">
			<h2 class="text-4xl lg:text-5xl font-bold text-white mb-4">Mis Servicios</h2>
			<p class="text-[#94a3b8] text-lg">Áreas de especialización en infraestructura informatique</p>
		</div>
		<div class="grid md:grid-cols-3 gap-8">
			{#each servicios as servicio}
				<div class="bg-[#1e3a5f]/50 rounded-2xl p-8 border border-[#3b82f6]/20 hover:border-[#3b82f6]/50 transition-all hover:scale-105">
					<div class="text-5xl mb-6">{servicio.icono}</div>
					<h3 class="text-2xl font-bold text-white mb-3">{servicio.titulo}</h3>
					<p class="text-[#94a3b8] mb-6">{servicio.descripcion}</p>
					<div class="flex items-center gap-2">
						<span class="text-3xl font-bold text-[#3b82f6]">{servicio.proyectos}</span>
						<span class="text-[#94a3b8]">Proyectos</span>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section id="sobre-mi" class="py-20">
	<div class="max-w-7xl mx-auto px-6">
		<div class="grid lg:grid-cols-2 gap-12">
			<div class="bg-[#1e3a5f]/30 rounded-2xl p-8 border border-[#3b82f6]/20">
				<h3 class="text-2xl font-bold text-white mb-4">Cualquier consulta o discusión</h3>
				<p class="text-[#94a3b8] mb-6">
					¿Tienes algún proyecto en mente o quieres conversar sobre infraestructura informatique?
					Estoy siempre abierto a discutir nuevas oportunidades y formas de colaborar.
				</p>
				<a href="#contacto" class="inline-flex items-center gap-2 text-[#3b82f6] font-medium hover:underline">
					Hablemos
					<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
				</a>
			</div>
			<div class="bg-gradient-to-br from-[#3b82f6]/20 to-[#06b6d4]/10 rounded-2xl p-8 border border-[#3b82f6]/20 flex items-center justify-center">
				<blockquote class="text-xl lg:text-2xl text-white font-medium italic text-center">
					"La creatividad no tiene límites. Cuanto más la usas, más tienes en tu mente."
				</blockquote>
			</div>
		</div>
	</div>
</section>

<section id="proyectos" class="py-20 bg-[#0f172a]">
	<div class="max-w-7xl mx-auto px-6">
		<div class="text-center mb-16">
			<h2 class="text-4xl lg:text-5xl font-bold text-white mb-4">Proyectos</h2>
			<p class="text-[#94a3b8] text-lg">Proyectos prácticos realizados durante mis estudios</p>
		</div>
		<div class="bg-[#1e3a5f]/50 rounded-2xl p-8 border border-[#3b82f6]/20">
			<div class="flex flex-col lg:flex-row gap-8">
				<div class="lg:w-1/3">
					<div class="bg-[#0a1628] rounded-xl p-6 flex items-center justify-center">
						<span class="text-7xl">🎮</span>
					</div>
				</div>
				<div class="lg:w-2/3">
					<h3 class="text-2xl font-bold text-white mb-3">Servidor Doméstico para Juegos</h3>
					<p class="text-[#94a3b8] mb-4">
						Construcción y operación de un servidor doméstico para alojar servidores de juegos
						como Minecraft y Counter-Strike. Incluye configuración de red, seguridad,
						mantenimiento y gestión de usuarios.
					</p>
					<div class="flex flex-wrap gap-2 mb-4">
						<span class="px-3 py-1 bg-[#3b82f6]/20 text-[#3b82f6] rounded-full text-sm">Linux</span>
						<span class="px-3 py-1 bg-[#3b82f6]/20 text-[#3b82f6] rounded-full text-sm">Docker</span>
						<span class="px-3 py-1 bg-[#3b82f6]/20 text-[#3b82f6] rounded-full text-sm">Redes</span>
						<span class="px-3 py-1 bg-[#3b82f6]/20 text-[#3b82f6] rounded-full text-sm">SSH</span>
						<span class="px-3 py-1 bg-[#3b82f6]/20 text-[#3b82f6] rounded-full text-sm">Minecraft Server</span>
					</div>
					<a href="https://github.com/MatiasPriguetti03" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 text-[#3b82f6] font-medium hover:underline">
						Ver en GitHub
						<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
					</a>
				</div>
			</div>
		</div>
	</div>
</section>

<section id="educacion" class="py-20">
	<div class="max-w-7xl mx-auto px-6">
		<div class="text-center mb-16">
			<h2 class="text-4xl lg:text-5xl font-bold text-white mb-4">Educación</h2>
			<p class="text-[#94a3b8] text-lg">Formación académica y certificaciones</p>
		</div>
		<div class="max-w-3xl mx-auto">
			<div class="bg-[#1e3a5f]/50 rounded-2xl p-8 border border-[#3b82f6]/20">
				<div class="flex items-start gap-6">
					<div class="w-16 h-16 bg-[#3b82f6]/20 rounded-xl flex items-center justify-center flex-shrink-0">
						<span class="text-3xl">🎓</span>
					</div>
					<div>
						<h3 class="text-2xl font-bold text-white mb-2">Analista en Infraestructura Informática</h3>
						<p class="text-[#06b6d4] font-medium mb-2">ORT Uruguay</p>
						<p class="text-[#94a3b8] mb-4">
							Carrera técnica enfocada en administración de sistemas, redes de computadoras,
							infraestructura cloud, virtualización y seguridad informática.
						</p>
						<div class="grid sm:grid-cols-3 gap-4 text-center">
							{#each estadisticas as stat}
								<div class="bg-[#0a1628] rounded-lg p-4">
									<span class="text-3xl font-bold text-[#3b82f6]">{stat.numero}</span>
									<p class="text-[#94a3b8] text-sm">{stat.etiqueta}</p>
								</div>
							{/each}
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<section id="contacto" class="py-20 bg-[#0f172a]">
	<div class="max-w-7xl mx-auto px-6">
		<div class="text-center mb-16">
			<h2 class="text-4xl lg:text-5xl font-bold text-white mb-4">Contacto</h2>
			<p class="text-[#94a3b8] text-lg">¿Te gustaría contactarme? ¡Adelante!</p>
		</div>
		<div class="max-w-2xl mx-auto">
			<div class="bg-[#1e3a5f]/50 rounded-2xl p-8 border border-[#3b82f6]/20">
				<div class="space-y-6">
					<a href="mailto:joaquin.escudero@email.com" class="flex items-center gap-4 p-4 bg-[#0a1628] rounded-xl hover:bg-[#3b82f6]/10 transition-colors group">
						<div class="w-12 h-12 bg-[#3b82f6]/20 rounded-lg flex items-center justify-center text-[#3b82f6] group-hover:bg-[#3b82f6]/30 transition-colors">
							<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
						</div>
						<div>
							<p class="text-[#94a3b8] text-sm">Email</p>
							<p class="text-white font-medium">joaquin.escudero@email.com</p>
						</div>
					</a>
					<a href="https://github.com/MatiasPriguetti03" target="_blank" rel="noopener noreferrer" class="flex items-center gap-4 p-4 bg-[#0a1628] rounded-xl hover:bg-[#3b82f6]/10 transition-colors group">
						<div class="w-12 h-12 bg-[#3b82f6]/20 rounded-lg flex items-center justify-center text-[#3b82f6] group-hover:bg-[#3b82f6]/30 transition-colors">
							<svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
						</div>
						<div>
							<p class="text-[#94a3b8] text-sm">GitHub</p>
							<p class="text-white font-medium">@MatiasPriguetti03</p>
						</div>
					</a>
				</div>
			</div>
		</div>
	</div>
</section>

<footer class="py-8 border-t border-[#1e3a5f]">
	<div class="max-w-7xl mx-auto px-6 text-center">
		<p class="text-[#94a3b8]">
			© 2024 Joaquin Escudero. Todos los derechos reservados.
		</p>
	</div>
</footer>
