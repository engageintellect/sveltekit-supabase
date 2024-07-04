<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import UpdateProfile from '$lib/components/UpdateProfile.svelte';

	const { data } = $props();
	const { userProfile } = data;
</script>

{#if userProfile}
	<UpdateProfile {userProfile} avatar={data?.user?.user_metadata.avatar_url} />
{:else}
	<Hero />
{/if}
