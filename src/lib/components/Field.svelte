<script>
    import { onMount } from "svelte";

    export let type
    export let name
    export let value

    onMount(() => {
        let item = document.querySelector("#"+name)
        item.type = item.getAttribute("data-type")
    })

</script>


<input id={name} 
    data-type={type} 
    {name} 
    placeholder={name} 
    bind:value={value} 
    required />