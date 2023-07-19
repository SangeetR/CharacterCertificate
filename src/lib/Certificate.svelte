<script>
    export let schoolName;
    export let certDate = Date.now();
    export let name = 'Sangeet';
    export let father = 'Mahesh';
    export let streamClass = '12th Science';
    export let doj;
    export let dol;
    export let sr;
    export let sex;
</script>

<div class="certificate">
    <div class="school">{schoolName}</div>
    <p class="cert">Character Certificate</p>
    <p class="date">Date : {certDate.toString()}</p>
    <div class="content">
        <p>It is certified that <strong> {name} </strong> {#if sex=='m'}Son {:else}Daughter{/if} of shree <strong> {father} </strong>, S.R. No. {sr} is a regular student during the year <strong> {doj} </strong> to <strong> {dol} </strong> and has passed class <strong> {streamClass} </strong> from this school.</p>
        <p>As per school record {#if sex=='m'}his{:else}her{/if} character and conduct is good to my knowledge.</p>
        <p>I wish {#if sex=='m'}his{:else}her{/if} success in future life.</p>
    </div>
    <p class="sign"><br><br>PRINCIPAL</p>
</div>

<style>
    .school 
    {
        font-size: 3em;
        padding: 10px;
        margin-top: 3%;
        line-height: 110%;
        /* font-family: 'Cinzel', serif; */
        font-family: 'Nanum Myeongjo', serif;
    }

    .cert 
    {
        /* font-size: 1.8em; */
        font-size: 2.5em;
        border: black solid 1px;
        padding: 7.5px;
        margin: 5% 20% 5% 20%;
        border-radius: 3px;
        /* font-family: "Times New Roman", Times, serif; */
        /* font-family: 'Libre Baskerville', serif; */
        font-family: 'Pirata One', cursive;
    }

    .date
    {
        text-align: right;
        font-size: 1.2em;
        
        font-family: 'Libre Baskerville', serif;
    }

    .certificate 
    {
        margin: 25px;
        border: solid black 2px;
        padding: 20px;
        border-radius: 5px;
    }

    .content
    {
        text-align: justify;
        font-size: 1.4em;
        line-height: 150%;
        /* font-family: "Times New Roman", Times, serif; */
        font-family: baskerville, serif;
    }

    .sign
    {
        text-align: right;
        font-size: 1.75em;
        margin-bottom: 0;
        padding-bottom: 0;
        font-family: 'Cinzel', serif;
    }
</style>