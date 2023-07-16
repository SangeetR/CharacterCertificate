<script>
    export let schoolName;
    export let certDate;
    export let name;
    export let father;
    export let streamClass;
    export let session;
    export let sex ="m";
    export let sr;
</script>

<div>
    <div>{schoolName}</div>
    <p>Character Certificate</p>
    <p>Date:{certDate}</p>
    <p>This is to certify that {name} {#if sex="m"}Son{:else}Daughter{/if} of shree {father} SR No. {sr} was a student of {streamClass} class during the session {session}.</p>
    <p>To the best of my knowledge, he/she bears a good moral character.</p>
    <p>Principal</p>
</div>