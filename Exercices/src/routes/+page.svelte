<script>
	import Exercise3 from './components/exercise3.svelte';
	import Exercise4 from './components/exercise4.svelte';
	import Exercise5 from './components/exercise5.svelte';
	import Exercise1 from './components/introduction.svelte';
	import Exercise2 from './components/reactivity.svelte';

	function toggle() {
		window.document.body.classList.toggle('dark-mode');
	}
</script>

<head>
	<title>Learning Svelte</title>
</head>
<body>
	<div class="d-flex align-items-start">
		<div
			class="nav flex-column nav-pills me-3"
			id="v-pills-tab"
			role="tablist"
			aria-orientation="vertical"
		>
			<button
				class="nav-link active"
				id="v-pills-e1-tab"
				data-bs-toggle="pill"
				data-bs-target="#v-pills-e1"
				type="button"
				role="tab"
				aria-controls="v-pills-e1"
				aria-selected="true">Introduction</button
			>
			<button
				class="nav-link"
				id="v-pills-e2-tab"
				data-bs-toggle="pill"
				data-bs-target="#v-pills-e2"
				type="button"
				role="tab"
				aria-controls="v-pills-e2"
				aria-selected="false">Reactivity</button
			>
			<button
				class="nav-link"
				id="v-pills-e3-tab"
				data-bs-toggle="pill"
				data-bs-target="#v-pills-e3"
				type="button"
				role="tab"
				aria-controls="v-pills-e2"
				aria-selected="false">Exercise 3</button
			>
			<button
				class="nav-link"
				id="v-pills-e4-tab"
				data-bs-toggle="pill"
				data-bs-target="#v-pills-e4"
				type="button"
				role="tab"
				aria-controls="v-pills-e4"
				aria-selected="false">Exercise 4</button
			>
			<button
				class="nav-link"
				id="v-pills-e5-tab"
				data-bs-toggle="pill"
				data-bs-target="#v-pills-e5"
				type="button"
				role="tab"
				aria-controls="v-pills-e5"
				aria-selected="false">Exercice 5</button
			>
			<button
				class="nav-link"
				type="button"
				style="background-color: yellowgreen;"
				on:click={toggle}>Design</button
			>
		</div>
		<div class="tab-content" id="v-pills-tabContent">
			<div
				class="tab-pane fade show active"
				id="v-pills-e1"
				role="tabpanel"
				aria-labelledby="v-pills-e1-tab"
				tabindex="0"
			>
				<Exercise1 />
			</div>
			<div
				class="tab-pane fade"
				id="v-pills-e2"
				role="tabpanel"
				aria-labelledby="v-pills-e2-tab"
				tabindex="0"
			>
				<Exercise2 />
			</div>
			<div
				class="tab-pane fade"
				id="v-pills-e3"
				role="tabpanel"
				aria-labelledby="v-pills-e3-tab"
				tabindex="0"
			>
				<Exercise3 />
			</div>
			<div
				class="tab-pane fade"
				id="v-pills-e4"
				role="tabpanel"
				aria-labelledby="v-pills-e4-tab"
				tabindex="0"
			>
				<Exercise4 />
			</div>
			<div
				class="tab-pane fade"
				id="v-pills-e5"
				role="tabpanel"
				aria-labelledby="v-pills-e5-tab"
				tabindex="0"
			>
				<Exercise5 />
			</div>
		</div>
	</div>
</body>

<style>
	:global(body) {
		background-color: #f2eee2;
		color: #0084f6;
		transition: background-color 0.3s;
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	}
	:global(body.dark-mode) .d-flex {
		background-color: #1d3040;
		color: white;
	}
	:global(body.dark-mode) button {
		background-color: #079cff;
		color: white;
	}
	button {
		font-size: 1.5em;
	}
</style>
