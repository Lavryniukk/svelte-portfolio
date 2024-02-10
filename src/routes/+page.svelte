<script lang="ts">
	import githubLogoSrc from '$lib/github-mark-white.png'
	import telegramLogoSrc from '$lib/telegram-logo.png'
	import instagramLogoSrc from '$lib/insta-grad.png'
	import meSrc from '$lib/me.png'
	let currentSection = 1;
	function changeSection(section: number){
		currentSection = section;
		
	}
</script>
<main class:showSection2={currentSection == 2} class:showSection1={currentSection == 1} class="flex  origin-bottom-right max-w-[100vw] max-h-[100vh] ">
	<section class="relative flex flex-col items-center justify-end w-screen h-screen bg-black">
		<div class="absolute top-[20%] w-[35%] left-[calc(50%-17.5%)] custom-shadow aspect-square border-[37px] border-red rounded-full "/>
		<picture class="z-50 ">
			<img src={meSrc} class="h-full" alt="Literally me">
		</picture>
		<div class='absolute flex items-center justify-center gap-5 left-10 top-10 '	>
			<figure class='w-20 h-20 border-[5px] border-white text-white flex items-center justify-center text-5xl font-serif font-bold rounded-full'>L</figure>
			<p class=" tracking-[0.4rem] text-2xl font-semibold text-red">LAVRYNIUK</p>
		</div>
		<div class='absolute right-10 top-10 '>
			<p class='text-4xl font-semibold tracking-widest text-right text-red '>LEV<br/> LAVRYNIUK</p>
		</div>
		<nav class='h-20 absolute rotate-90 -right-[11%] w-[30%] top-[calc(50%-40px)] flex  justify-between  '>
		<button on:click={()=>changeSection(2)}>ABOUT</button><button >PROJECTS</button><button>CONTACT</button>
		</nav>
		<ul class="absolute flex items-center justify-center gap-4 bottom-10 right-10">
			<li><a href='https://github.com/Lavryniukk'><img src={githubLogoSrc} alt=""></a></li>
			<li><a href='https://t.me/llavryniuk'><img src={telegramLogoSrc} alt=""></a></li>
			<li><a href='https://www.instagram.com/llavryniuk/'><img src={instagramLogoSrc} alt=""></a></li>
		</ul>
		<div class='absolute flex flex-col items-end font-semibold bottom-10 left-10'>
			<h2 class="text-3xl text-white">Web Engineer</h2>
			<p class="flex items-center justify-end gap-2 font-medium text-gray-400">at <span class="text-red mb-0.5 text-right text-2xl"><a  class='hover:underline' href='https://cleverize.co'>Cleverize.co</a></span></p>
		</div>
	</section>
	<section class="flex w-[99vw]  h-[99vh] left-[100vw] absolute origin-bottom-left  rotate-90   border-2 border-black -translate-y-[calc(99vw-8px)] ">
		<div class="relative z-50 flex items-center justify-center w-full h-full gap-10 p-20 bg-black">
		<div class="absolute -top-[500px] -right-[500px] custom-shadow w-[1000px] h-[1000px]  rounded-full  border-[30px] border-red "></div>
		<button class="absolute flex flex-col items-center justify-center text-lg text-red bottom-10 left-10" on:click={()=>changeSection(1)}>Back <div class="rotate-90">{`->`}</div></button>
		<div class="flex flex-col items-center justify-center gap-10">
			<div class="flex items-center justify-center ">
				<div class="  gap-10 border-l-2 border-l-red w-[500px] flex-col h-fit flex p-4">
					<h1 class="text-3xl font-semibold tracking-widest text-red ">ABOUT ME</h1>
					<p class="text-xl font-light text-white/80">My name is Lev, i am from Ukraine.<br/>
					I have been writing code since very young age, and i am still in love with it.
					I love the feeling of creating something from nothing, and i love the feeling of solving problems.
					It makes me happy to see how my code is being used by people, and how it helps them to solve their problems.
					</p>
				</div>
				<div class="  gap-10 border-l-2 border-l-red w-[500px] flex-col h-fit flex p-4">
					<h1 class="text-3xl font-semibold tracking-widest text-red ">MY EXPERIENCE</h1>
					<p class="text-xl font-light text-white/80">
						I have built several things from scratch, from simple landing pages, to complex web applications with multilevel architecture.
						I can do both frontend and backend, but i prefer to work on the frontend, because i enjoy the process of creating beautiful and user-friendly interfaces.
					</p>
				</div>
			</div>
			<div class="flex items-center justify-center ml-[50%] ">
			<div class="  gap-10 border-l-2 border-l-red w-[500px] flex-col h-fit flex p-4">
				<h1 class="text-3xl font-semibold tracking-widest text-red ">MY PROJECTS</h1>
				<p class="text-xl font-light text-white/80">
					Most of my projects are private, because client want them that way,  but i have some public projects on <a class="italic font-bold underline" href='https://github.com/lavryniukk'>my github</a>, you can check them out.
				</p>
			</div>
			<div class="  gap-10 border-l-2 border-l-red w-[500px] flex-col h-fit flex p-4">
				<h1 class="text-3xl font-semibold tracking-widest text-red ">HOW TO REACH ME</h1>
				<p class="text-xl font-light text-white/80">
					There are links on the front page, you can use them to reach me, or you can just write an email to <a class="italic font-bold underline" href='mailto:leoyt109@gmail.com'>Me</a>
				</p>
			</div>
		</div>
		</div>
		

		</div>
	</section>



</main>

<style>
	.showSection1{
		@apply transition-all duration-1000 -rotate-0
	}
	.showSection2{
		@apply transition-all duration-1000 -rotate-90
	}
	
	.custom-shadow {
	  box-shadow: 0px 0px 100px -10px #E40037, inset 0px 0px 100px -10px #E40047;
	}
	nav button {
		@apply  text-white font-semibold text-2xl tracking-widest
	}
	ul li img {
		@apply w-8 h-8
	}
  </style>