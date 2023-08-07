<!-- header -->

<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
</script>

<header class="flex flex-row  items-center justify-between px-20 ">
	<div class=''>
		<a href="https://kit.svelte.dev">
			<img src={logo} alt="SvelteKit" class="h-12 w-12" />
		</a>
	</div>

	<nav>
		
		<ul class='flex flex-row gap-3 text-3xl font-semibold uppercase '>
			<li class="hover:underline hover:text-yellow-300" aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			
			
		</ul>
		
	</nav>

	<div class="corner">
		<a href="https://github.com/sveltejs/kit">
			<img src={github} alt="GitHub" class="h-12 w-12" />
		</a>
	</div>
</header>


