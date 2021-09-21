<script>
  import Student from './Student.svelte';
  let students = [
    {
      name: 'Karthik',
      age: 19,
      course: 'maths, science, english',
      id: 1,
    },
    {
      name: 'Suman',
      age: 16,
      course: 'maths, science, english, sanskrit',
      id: 2,
    },
    {
      name: 'Janhavi',
      age: 20,
      course: 'maths, science, kannada',
      id: 3,
    },
    {
      name: 'Raghu',
      age: 22,
      course: 'maths, english, hindi',
      id: 4,
    },
  ];
	let filteredStudents = []
  const filterStudents = (e) => {
 		return filteredStudents = students.filter((student) => {
      return student.name.toLowerCase().includes(e.target.value.toLowerCase());
    });
  };
</script>

<div>
  <input type="text" on:input={filterStudents} />

	{#if filteredStudents.length === 0}
		 {#each students as student}
    <Student {student} />
  {/each}
	{:else if filteredStudents.length > 0}
	{#each filteredStudents as student}
    <Student {student} />
  {/each}
	{:else}
	<h4>No Results Found</h4>
	{/if}
 
</div>

<style>
</style>
