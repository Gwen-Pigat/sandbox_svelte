<script>

    export let type
    export let name
    export let value

</script>


<input id={name} 
    {...{ type }}
    {name} 
    placeholder={name} 
    bind:value={value} 
    required />