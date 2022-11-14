<template>
  <div class="students">
    <h1>Students</h1>
    <div class="table-responsive">
      <table
        class="table table-hover table-fixedheader table-striped table-bordered table-dark"
      >
        <thead class="thead-light">
          <tr>
            <th scope="col">#</th>
            <th scope="col">First</th>
            <th scope="col">Last</th>
            <th scope="col">Age</th>
            <th scope="col">Date of Enrollment</th>
            <th scope="col">Grade</th>
            <th scope="col">GPA</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(student, index) in students" :key="student.studentId">
            <th scope="row">{{ index + 1 }}</th>
            <td>{{ student.fname }}</td>
            <td>{{ student.lname }}</td>
            <td>{{ student.age }}</td>
            <td>{{ student.dateOfEnrollment }}</td>
            <td>{{ student.grade }}</td>
            <td>{{ student.gpa }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      students: {
        studentId: 0,
        fname: "",
        lname: "",
        age: "",
        dateOfEnrollment: "",
        grade: "",
        gpa: "",
      },
    };
  },
  mounted() {
    try {
      axios.get("https://localhost:5001/api/Student").then((response) => {
        this.students = response.data.value;
        console.log(this.students);
      });
    } catch (err) {
      console.log(err);
    }
  },
};
</script>
