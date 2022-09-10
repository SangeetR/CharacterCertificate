<script>
    export let schoolName;
    export let certDate = Date.now();
    export let name = 'Sangeet';
    export let father = 'Mahesh';
    export let streamClass = '12th Science';
    export let doj;
    export let dol;
</script>

<div class="certificate">
    <div class="school">{schoolName}</div>
    <p class="cert">Character Certificate</p>
    <p class="date">Date : {certDate.toString()}</p>
    <div class="content">
        <p>It is certified that <strong> {name} </strong> Son/Daughter of shree <strong> {father} </strong> was a regular student during the year <strong> {doj} </strong> to <strong> {dol} </strong> and has passed class <strong> {streamClass} </strong> from this school.</p>
        <p>As per school record his/her character and conduct is good to my knowledge.</p>
        <p>I wish his/her success in future life.</p>
    </div>
    <p class="sign"><br><br>PRINCIPAL</p>
</div>

<style>
    .school 
    {
        font-size: 2.2em;
        padding: 10px;
        margin-top: 3%;
        line-height: 110%;
        font-family: 'Cinzel', serif;
    }

    .cert 
    {
        font-size: 1.8em;
        border: black solid 1px;
        padding: 7.5px;
        margin: 5% 20% 5% 20%;
        border-radius: 3px;
        font-family: 'Libre Baskerville', serif;
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
        font-family: 'Libre Baskerville', serif;
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