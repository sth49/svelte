<script>
    export let checked = false;
    export let name = 'x-encoding';
    export let value;
    export let id;
</script>

<div class='form-check form-check-inline'>

{#if checked}
    <input checked class='form-check-input' type="radio" name={name} value={value} id={id}/>
{:else}
    <input class='form-check-input' type="radio" name={name} value={value} id={id}/>
{/if}
<label class='form-check-label' for="selector">{value}</label>
</div>