<script>
	import Header from '../components/Header.svelte';
	import Cards from '../components/Cards.svelte';
	import Overview from '../components/Overview.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<style>
	:global(:root) {
		--bg: hsl(230, 17%, 14%);
		--top-bg: hsl(232, 19%, 15%);
		--text: hsl(228, 34%, 66%);
		--text-tl: hsl(0, 0%, 100%);
		--card: hsl(228, 28%, 20%);
		--hover: hsl(228, 28%, 25%);
		--border-top: 1px solid hsl(228, 34%, 66%);
		--transform: translateX(0);
		--toggle: linear-gradient(to right, hsl(210, 78%, 56%), hsl(146, 68%, 55%));
		--shadow: 0px 3px 4px 0px hsl(228, 28%, 14%);
	}

	:global(body) {
		background-color: var(--bg);
		color: var(--text);
	}

	:global(h1, h2, h3) {
		color: var(--text-tl);
	}

	:global(body.light-mode) {
		--bg: hsl(0, 0%, 100%);
		--top-bg: hsl(225, 100%, 98%);
		--text-tl: hsl(230, 17%, 14%);
		--text: hsl(228, 12%, 44%);
		--card: hsl(227, 47%, 96%);
		--hover: hsl(227, 47%, 91%);
		--border-top: 1px solid hsl(230, 22%, 74%);
		--transform: translateX(24px);
		--toggle: hsl(230, 22%, 74%);
		--shadow: 0px 2px 4px 0px hsl(227, 47%, 96%);
	}
</style>

<svelte:head>
	<title>Social Media Dashboard</title>
</svelte:head>

<Header />
<Cards />
<Overview />
<Footer />