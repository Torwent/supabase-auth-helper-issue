<script lang="ts">
	export let data;
	$: ({ session } = data);
</script>

<h1>Welcome to SvelteKit</h1>
{#if session}
	You are logged in! Your id is: {session.user.id}
{:else}
	You are logged out!
{/if}
<form method="POST" class="card variant-filled-surface p-4">
	<button formaction="/?/login&provider=discord"> Login with Discord </button>
	<button formaction="/?/logout">Logout</button>
</form>
