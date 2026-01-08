<script lang="ts">
</script>

<header>
	<h1>Bulk Email Sender</h1>
	<nav>
		<a href="/login">Login</a>
		<a href="/dashboard">Dashboard</a>
	</nav>
</header>

<main>
	<slot />
</main>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 12px 20px;
		border-bottom: 1px solid #ddd;
	}

	nav a {
		margin-left: 12px;
		text-decoration: none;
		color: #333;
	}
</style>
