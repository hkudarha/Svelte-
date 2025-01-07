<script>
    import { getContext } from "svelte";
    const username = getContext('username-context')
</script>
<h2>Child D component</h2>
<h2> child D username -{username}</h2>