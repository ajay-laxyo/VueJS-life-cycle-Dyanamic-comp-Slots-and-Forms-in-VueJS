<template>
	<div>
		<!-- <h1> this msg from Student component :- <u> {{ message }} </u></h1>
		<h2> {{ myMsg }} </h2>
		<slot name="myNew"></slot>
 -->
		<!-- <form>
			<div id="form-header">
				<slot name="form-header"></slot>
			</div>
			<div id="form-element">
				<slot name="form-element"></slot>
			</div>
			<div id="form-button">
				<slot name="form-button"></slot>
			</div>
			<div id="form-footer">
				<slot name="form-footer"></slot>
			</div>
		</form> -->

		<form>
			<h2> This is Student Form</h2>
			<p>
				<label>Name </label><br>
				<input type="text" v-model.lazy="std.name" name="stdName">
			</p>
			<p>
				<label>Class </label><br>
				<input type="text" v-model.lazy="std.class" name="stdClass">
			</p>
			<p>
				<label>Roll Number </label><br>
				<input type="text" v-model.lazy="std.roll_no" name="stdRollNo">
			</p>
			<p>
				<label> Branch </label><br>
				<input type="radio" value="CSE" v-model="std.branch"> CSE
				<input type="radio" value="IT" v-model="std.branch"> IT
				<input type="radio" value="EC" v-model="std.branch"> EC
				<!-- <input type="text" v-model.lazy="std.branch" name="stdBranch"> -->
			</p>
			<p>
				<button >Submit</button>
			</p>
		</form>
		<hr>
		<div id="detail-preview" style="background-color: #ffcccc;">
			<h3>Details Preview</h3>
			<p>Name : {{std.name}} </p>
			<p>Class : {{std.class}} </p>
			<p>Roll no. : {{std.roll_no}} </p>
			<p>Branch : {{std.branch}} </p>
		</div>
	</div>
</template>

<script>
	export default {
		props : ["myMsg"],
		data() {
			return {
				message : "Hii this is Student component",
				std:{
					name:"",
					class:"",
					roll_no:"",
					branch:""
				}
			}
		},
		methods:{

		},
		computed:{

		}
	}
</script>