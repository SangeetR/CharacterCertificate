<script>
  import Certificate from "./lib/Certificate.svelte";

  let students = [
  ];

  let schoolName = 'Rathi Public Sr. Sec. School Dhawas, Ajmer Road Jaipur';
  let certDate;
  let name;
  let father;
  let streamClass;
  let doj;
  let dol;
  let one;
  let sr;
  let sex;

  const addCertificate = () => 
  {
    const student = {name, father, doj, dol, streamClass, sr, sex};
    students = [student, ...students]
    one.focus()
  }
  
  const delStu = (i) => {
    students.splice(i,1);
    students = students;
  }
</script>

<main>
  <form on:submit|preventDefault={addCertificate} class="no-print">

    <fieldset>
      <legend>Common Details</legend>
      
      <label for="schoolName">School Name</label>
      <input type="text" name="schoolName" id="schoolName" bind:value={schoolName}>

      <label for="certDate">Date of Certificate Issue</label>
      <input type="text" name="certDate" id="certDate" bind:value={certDate}>
    </fieldset>
    
    <label for="name" bind:this={one}>Name:</label>
    <input type="text" name="name" id="name" bind:value={name}>
    
    <label for="father">Father's Name:</label>
    <input type="text" name="father" id="father" bind:value={father}>
    
    <br>
    <!-- <label for="dob">Date of Birth</label>
    <input type="date" name="dob" id="dob" bind:value={dob}> -->
    
    <label for="doj">Date of Admission</label>
    <input type="text" name="doj" id="doj" bind:value={doj}>
    
    <label for="dol">Date of Result</label>
    <input type="text" name="dol" id="dol" bind:value={dol}>

    <br>
    <label for="streamClass">Class(Stream)</label>
    <input type="text" name="streamClass" id="streamClass" bind:value={streamClass}>

    <label for="sr">S.R. Number</label>
    <input type="text" name="sr" id="sr" bind:value={sr}>

    <br>
    <label for="sex">Sex</label>
    <select bind:value={sex} name="sex" id="sex">
      <option value="m">Male</option>
      <option value="f">Female</option>
    </select>
    
    <br>
    <button type="submit">Add Student</button>

  </form>
  <table class="no-print">
    <tr>
      <th>Serial</th>
      <th>SR No.</th>
      <th>Name</th>
      <th>Father's Name</th>
      <th>Date of Admission</th>
      <th>Result Date</th>
      <th>Sex</th>
      <th></th>
    </tr>
    
    {#each students as student, i}
      <tr>
        <td>{i+1}</td>
        <td>{student.sr}</td>
        <td>{student.name}</td>
        <td>{student.father}</td>
        <td>{student.doj}</td>
        <td>{student.dol}</td>
        <td>{student.sex}</td>
        <td class="del" on:click= {()=> {delStu(i)} }>Delete</td>
      </tr>
    {/each}

  </table>
  <!-- {#each students as student}
    
  {/each} -->
  <div class="to-print">
    {#each students as student}
      <div class="break-after">
        <Certificate
           {schoolName}
          {certDate}
          name = {student.name}
          father = {student.father}
          streamClass = {student.streamClass}
          doj = {student.doj}
          dol = {student.dol}
          sr= {student.sr}
          sex={student.sex}
        />
      </div>
    {/each}
  </div>
</main>

<style>

  form 
  {
    padding: 20px;
  }

  button 
  {
    margin: 15px;
  }

  input 
  {
    margin: 10px;
    font-size: larger;
  }

  label
  {
    font-size: larger;
  }

  @media print 
  {
    .no-print
    {
      visibility: hidden;
    }
    
    .to-print
    {
      position: absolute;
      float:none;
      top: 10px;
      left: 10px;
    }

    .break-after
    {
      page-break-after: always;
    }
  }

  /* CSS Snippet For Responsive Table - Basic */

* {
  box-sizing: border-box;
}

table {
  border-spacing: 0px;
  border-collapse: collapse;
  width: 100%;
  max-width: 100%;
  margin-bottom: 15px;
  background-color: transparent; /* Change the background-color of table here */
  text-align: left; /* Change the text-alignment of table here */
}

th {
  font-weight: bold;
  border: 1px solid #cccccc; /* Change the border-color of heading here */
  padding: 8px;
}

td {
  border: 1px solid #cccccc; /* Change the border-color of cells here */
  padding: 8px;
}
</style>
