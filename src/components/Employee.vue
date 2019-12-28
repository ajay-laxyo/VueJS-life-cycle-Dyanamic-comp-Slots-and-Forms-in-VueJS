<template>
	<div>
		<h3> this msg from Employee component :- <u> {{ message }} </u></h3>
		<br>
		
		<form>
			<h2> This is Employee Form</h2>
			<p>
				<label>Name </label><br>
				<input type="text" v-model.lazy="emp.name" name="empName">
			</p>
			<p>
				<label>Designation </label><br>
				<select v-model="emp.designation">
					<option v-for="designation in designations"> {{ designation }} </option>
				</select>
				<!-- <input type="text" v-model.lazy="emp.designation" name="empDesign"> -->
			</p>
			<p>
				<label><input type="checkbox" v-model="emp.post" value="Developer"> Developer </label>
				<label><input type="checkbox" v-model="emp.post" value="Designer"> Designer</label>
				<label><input type="checkbox" v-model="emp.post" value="Tester"> Tester </label>
				<label><input type="checkbox" v-model="emp.post" value="CEO"> CEO </label>
				<!-- <input type="text" v-model.lazy="emp.post" name="empPost"> -->
			</p>
			<p>
				<label>Employee At </label><br>
				<input type="text" v-model.lazy="emp.emp_at" name="empAt">
			</p>
			<p>
				<button >Submit</button>
			</p>
		</form>
		<hr>
		<div id="detail-preview" style="background-color: #ffcccc;">
			<h3>Details Preview</h3>
			<p>Name : {{emp.name}} </p>
			<p>Designation : {{emp.designation}} </p>
			<p>Post : 
				<ul>
					<li v-for="p in emp.post"> {{p}} </li>
				</ul> 
			</p>
			<p>Employee At : {{emp.emp_at}} </p>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				message : "Hii this is Employee component",
				emp:{
					name:"",
					designation:"",
					post:[],
					emp_at:""
				},
				designations : ["PHP", "JAVA", "Oracal", "Python", "R"]
			}
		},
		methods:{

		},
		computed:{
			
		}
	}
</script>