<script lang="ts">
	let mdRendered: any;
	const loadData = async () => {
		const mdGlob = import.meta.glob('../mds/*.md');
        const mdFile = '15-Form-of-At-Will-Employment-Agreement';
        const mdContent: any = await mdGlob?.[`../mds/${mdFile}.md`]();
		mdRendered = mdContent.default;
	};
	loadData();
</script>

<section>
	<svelte:component this={mdRendered} />
</section>
