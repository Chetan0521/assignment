<script lang="ts">
	let email = '';
	let password = '';
	let loading = false;
	let error = '';
	
	function handleSubmit() {
		error = '';
		loading = true;

		// backend connection will be added later
		setTimeout(() => {
			loading = false;

			if (!email || !password) {
				error = 'Please fill in all fields';
			}
		}, 500);
	}
</script>

<h2>Login</h2>

<form on:submit|preventDefault={handleSubmit}>
	<div class="field">
		<label>Email</label>
		<input type="email" bind:value={email} />
	</div>

	<div class="field">
		<label>Password</label>
		<input type="password" bind:value={password} />
	</div>

	{#if error}
		<p class="error">{error}</p>
	{/if}

	<button type="submit" disabled={loading}>
		{loading ? 'Logging in...' : 'Login'}
	</button>
</form>

<style>
	form {
		max-width: 360px;
		margin-top: 20px;
	}

	.field {
		display: flex;
		flex-direction: column;
		margin-bottom: 12px;
	}

	input {
		padding: 8px;
		border: 1px solid #ccc;
		border-radius: 4px;
	}

	button {
		margin-top: 10px;
		padding: 8px;
		cursor: pointer;
	}

	.error {
		color: red;
		margin-top: 8px;
	}
</style>
