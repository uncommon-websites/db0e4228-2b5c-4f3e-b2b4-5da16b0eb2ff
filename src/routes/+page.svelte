<script lang="ts">
	import Header from "$lib/components/Header.svelte";
	import { ArrowUpRight, ArrowRight } from 'lucide-svelte';

	const services = [
		{ id: '01', name: 'SIGNATURE HAIRCUT' },
		{ id: '02', name: 'CLASSIC SHAVE' },
		{ id: '03', name: 'BEARD TRIM & STYLING' },
		{ id: '04', name: 'FADE & TAPER' },
		{ id: '05', name: 'HAIR STYLING' },
		{ id: '06', name: 'HOT TOWEL TREATMENT' },
		{ id: '07', name: 'GROOMING CONSULTATION' }
	];

	const team = [
		{ name: 'SINA', role: 'MASTER BARBER', img: '/generated/image-skilled-barber-in-black-apron-working-on-1765990990376-5.webp' },
		{ name: 'MARKO PETROVIĆ', role: 'SENIOR BARBER', img: '/generated/image-young-professional-barber-trimming-beard-1765990997391-6.webp' },
		{ name: 'NIKOLA JOVIĆ', role: 'BARBER', img: '/generated/image-experienced-barber-giving-classic-gentle-1765991005322-7.webp' }
	];
</script>

<div class="min-h-screen bg-[#F4F4F2] text-[#1A1A1A] font-sans selection:bg-primary-600 selection:text-white overflow-x-hidden">
	<Header />

	<main>
		<!-- Hero Section -->
		<section class="pt-12 md:pt-20 pb-10 px-4 md:px-8">
			<div class="flex flex-col md:flex-row justify-between items-start mb-12 md:mb-24 relative">
				<div class="max-w-[200px] text-[10px] leading-relaxed uppercase tracking-wide font-medium mt-2">
					<p>Premium men's barbershop in Banja Luka delivering exceptional haircuts through selective clientele and meticulous craftsmanship.</p>
				</div>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right mt-8 md:mt-0 uppercase">
					Where <br />
					Precision
				</h1>
			</div>

			<!-- Hero Images -->
			<div class="grid grid-cols-5 gap-2 md:gap-4 mb-8 h-[30vh] md:h-[50vh]">
				<div class="overflow-hidden h-full">
					<img src="/generated/image-professional-barbers-hands-carefully-tri-1765990935285-0.webp" alt="Barber hands trimming hair" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-close-up-of-a-straight-razor-being-sharp-1765990948370-1.webp" alt="Straight razor on strop" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-well-groomed-man-with-fresh-haircut-look-1765990964082-2.webp" alt="Client with fresh haircut" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-barber-applying-hot-towel-to-clients-fac-1765990975639-3.webp" alt="Hot towel shave" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-professional-barber-styling-clients-hair-1765990983491-4.webp" alt="Hair styling" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
			</div>

			<div class="flex flex-col md:flex-row justify-between items-start">
				<span class="text-[10px] uppercase tracking-wide font-medium mt-4 hidden md:block">Scroll</span>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right w-full uppercase">
					Meets <br />
					Excellence
				</h1>
			</div>
		</section>

		<!-- Services Section -->
		<section class="py-20 md:py-32" id="services">
			<div class="flex justify-center mb-16 md:mb-24">
				<span class="text-[10px] font-bold uppercase tracking-widest">Services</span>
			</div>

			<div class="border-t border-gray-300">
				{#each services as service}
					<div class="group border-b border-gray-300 py-6 md:py-10 px-4 md:px-8 flex items-center justify-between hover:bg-white transition-colors cursor-pointer">
						<span class="text-[10px] font-medium text-gray-500 w-8 md:w-12">/{service.id}</span>
						<h2 class="text-3xl md:text-6xl lg:text-7xl font-thin tracking-tight group-hover:italic transition-all duration-300 uppercase">{service.name}</h2>
						<div class="flex items-center gap-1 text-[10px] font-medium uppercase opacity-0 group-hover:opacity-100 transition-opacity translate-x-[-10px] group-hover:translate-x-0 duration-300">
							<ArrowUpRight size={12} />
							Book
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- Team Section -->
		<section class="py-20 px-4 md:px-8 bg-[#F4F4F2]" id="team">
			<div class="flex flex-col md:flex-row justify-between items-start mb-16 md:mb-24">
				<h2 class="text-4xl md:text-6xl font-light tracking-tight mb-8 md:mb-0 uppercase">Master Barbers</h2>
				<div class="max-w-xs text-[10px] leading-relaxed uppercase tracking-wide font-medium text-right md:text-left">
					<p>Our team consists of highly skilled barbers dedicated to the craft. Each cut is a work of art, each client receives undivided attention.</p>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-12 md:gap-y-16">
				{#each team as member}
					<div class="group cursor-pointer">
						<div class="aspect-[3/4] overflow-hidden mb-4 bg-gray-200">
							<img src={member.img} alt={member.name} class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-500" />
						</div>
						<h3 class="text-xs font-bold uppercase tracking-wide mb-1">{member.name}</h3>
						<p class="text-[10px] text-gray-500 uppercase tracking-wide mb-3">{member.role}</p>
						<div class="inline-flex items-center gap-1 text-[10px] font-medium uppercase opacity-0 group-hover:opacity-100 transition-opacity">
							<ArrowUpRight size={10} />
							Explore
						</div>
					</div>
				{/each}
				
				<!-- Book Appointment Card -->
				<div class="flex flex-col justify-between h-full min-h-[300px] border border-gray-300 p-8 bg-[#F4F4F2] hover:bg-white transition-colors cursor-pointer group">
					<div class="flex justify-center items-center flex-1">
						<ArrowRight size={48} class="text-gray-300 group-hover:text-black transition-colors" />
					</div>
					<div>
						<h3 class="text-xs font-bold uppercase tracking-wide mb-1 leading-relaxed">Ready for your<br/>transformation?</h3>
						<div class="inline-flex items-center gap-1 text-[10px] font-medium uppercase mt-4">
							<ArrowUpRight size={10} />
							Book Now
						</div>
					</div>
				</div>
			</div>
		</section>

		<!-- Shop Section -->
		<section class="py-20 px-4 md:px-8" id="shop">
			<div class="flex flex-col lg:flex-row mb-16 gap-12 lg:gap-24">
				<div class="flex-1">
					<h2 class="text-4xl md:text-6xl font-light tracking-tight uppercase">The Shop</h2>
				</div>
				<div class="flex-1">
					<h2 class="text-3xl md:text-5xl font-light tracking-tight mb-8 text-left uppercase leading-tight">Where tradition<br/>meets excellence</h2>
					<div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-[10px] leading-relaxed uppercase tracking-wide font-medium">
						<p>Sina Master Cut is Banja Luka's premier destination for discerning gentlemen who demand nothing but the finest in grooming. Our selective approach ensures every client receives undivided attention.</p>
						<p>We combine time-honored barbering techniques with modern precision. From classic cuts to contemporary fades, hot towel shaves to beard sculpting, every service is executed with meticulous attention to detail in our refined environment.</p>
					</div>
					<a href="#book" class="inline-flex items-center gap-1 text-[10px] font-medium uppercase mt-8 hover:opacity-60 transition-opacity">
						<ArrowUpRight size={10} />
						Book Appointment
					</a>
				</div>
			</div>

			<div class="flex flex-col md:flex-row gap-4 h-[50vh] md:h-[70vh]">
				<div class="w-full md:w-[60%] h-full bg-gray-200 overflow-hidden">
					<img src="/generated/image-modern-upscale-barbershop-interior-with--1765991012097-8.webp" alt="Barbershop Interior" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
				</div>
				<div class="w-full md:w-[40%] h-full flex flex-col gap-4">
					<div class="flex-1 bg-gray-200 overflow-hidden">
						<img src="/generated/image-elegant-barbershop-waiting-area-with-com-1765991017609-9.webp" alt="Waiting Area" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
					</div>
					<div class="flex-1 flex gap-4">
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="/generated/image-premium-grooming-products-displayed-on-w-1765991025510-10.webp" alt="Premium Products" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="/generated/image-vintage-barber-tools-and-scissors-arrang-1765991030725-11.webp" alt="Barber Tools" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
					</div>
				</div>
			</div>
		</section>

		<!-- CTA Section -->
		<section class="py-32 px-4 md:px-8 bg-[#1A1A1A] text-white text-center" id="book">
			<span class="text-[10px] font-medium uppercase tracking-widest mb-6 block opacity-80">Experience Premium Grooming</span>
			<h2 class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mb-12 uppercase">
				Ready for your <br />
				transformation?
			</h2>
			<a href="#contact" class="inline-block bg-primary-600 text-white px-10 py-4 rounded-full text-[10px] font-bold uppercase tracking-widest hover:bg-primary-700 transition-colors">
				Book Appointment
			</a>
		</section>

		<!-- Bottom Gallery -->
		<div class="grid grid-cols-2 md:grid-cols-5 h-[60vh]" id="gallery">
			<div class="overflow-hidden">
				<img src="/generated/image-barber-giving-detailed-beard-trim-with-s-1765991035944-12.webp" alt="Beard trim" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-client-getting-luxury-hot-towel-shave-tr-1765991042474-13.webp" alt="Hot towel shave" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-professional-barber-creating-perfect-fad-1765991047268-14.webp" alt="Fade haircut" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-satisfied-affluent-client-admiring-fresh-1765991051946-15.webp" alt="Client satisfaction" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden hidden md:block">
				<img src="/generated/image-barber-styling-clients-hair-with-pomade--1765991057964-16.webp" alt="Hair styling" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
		</div>

		<!-- Footer Marquee -->
		<div class="overflow-hidden py-6 border-b border-gray-200">
			<div class="whitespace-nowrap animate-marquee flex">
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Precision meets excellence — Where precision meets excellence — Where precision meets excellence — </span>
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Precision meets excellence — Where precision meets excellence — Where precision meets excellence — </span>
			</div>
		</div>
	</main>

	<footer class="px-4 md:px-8 py-12 text-[10px] font-medium uppercase tracking-wide" id="contact">
		<div class="flex flex-col md:flex-row justify-between items-start md:items-end gap-12 md:gap-8">
			<div class="flex flex-col gap-3">
				<a href="#services" class="hover:opacity-60">Services</a>
				<a href="#team" class="hover:opacity-60">Team</a>
				<a href="#shop" class="hover:opacity-60">Shop</a>
				<a href="#gallery" class="hover:opacity-60">Gallery</a>
				<a href="#book" class="hover:opacity-60">Book</a>
			</div>

			<div class="text-left md:text-center">
				<p class="text-xl md:text-3xl font-normal tracking-tight mb-2">+387 65 XXX XXX</p>
				<p class="text-lg md:text-2xl font-normal tracking-tight mb-6">INFO@SINAMASTERCUT.COM</p>
				<p class="text-lg tracking-widest">BANJA LUKA</p>
			</div>

			<div class="flex flex-col gap-3 text-left md:text-right">
				<a href="#privacy" class="hover:opacity-60">Privacy Policy</a>
				<a href="#terms" class="hover:opacity-60">Terms & Conditions</a>
			</div>
		</div>

		<div class="flex flex-col md:flex-row justify-between items-center mt-20 pt-8 border-t border-gray-200 text-[10px] text-gray-400 gap-4">
			<p>©SINA MASTER CUT. ALL RIGHTS RESERVED</p>
			<div class="flex items-center gap-1">
				<span class="text-black text-lg font-bold tracking-tight">SINA MASTER CUT</span>
			</div>
			<p>BANJA LUKA, BOSNIA AND HERZEGOVINA</p>
		</div>
	</footer>
</div>

<style>
	@keyframes marquee {
		0% { transform: translateX(0); }
		100% { transform: translateX(-50%); }
	}
	.animate-marquee {
		animation: marquee 30s linear infinite;
	}
</style>

