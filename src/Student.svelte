<script>
  export let student;
</script>

<div class="student">
  <h3 class="name">Name: {student.name}</h3>
  <p class="age">Age: {student.age}</p>
  <p class="course">Course: {student.course}</p>
</div>

<style>
  	.student {
		border: 3px solid goldenrod;
    margin-bottom: 30px;
    text-align: center;
    padding: 1rem;
	}

  .name {
  color: skyblue;
  }

  .age {
color: maroon;
  }

  .course {
    color: orange;
  }
</style>