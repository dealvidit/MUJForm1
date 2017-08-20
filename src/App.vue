<template>
	<div id="app">
		<div class="phone-viewport">
			<md-toolbar>
				<md-button class="md-icon-button" @click="toggleLeftSidenav">
					<md-icon>menu</md-icon>
				</md-button>

				<h2 class="md-title">Manipal Job Application Form</h2>
			</md-toolbar>
		</div>

		<md-sidenav class="md-left" ref="leftSidenav" @open="open('Left')" @close="close('Left')">
			<md-toolbar class="md-large">
				<div class="md-toolbar-container">
					<h3 class="md-title">Context Menu</h3>
				</div>
			</md-toolbar>

			<p>MADE WITH LOVE BY VIDIT MATHUR [161104040 - BCA III SEM]</p>
		</md-sidenav>

		<md-stepper>
			<md-step md-label="STEP 1" md-message="Application Information">
				<form novalidate @submit.stop.prevent="submit">
					<md-input-container>
						<label>Name of the Candidate</label>
						<md-input required v-model="initialValue"></md-input>
					</md-input-container>

					<md-input-container>
						<label>Specialization</label>
						<md-select name="movie" id="movie">
							<md-option value="fight_club">X</md-option>
							<md-option value="godfather">Y</md-option>
							<md-option value="godfather_ii">Z</md-option>
							<md-option value="godfather_iii">A</md-option>
							<md-option value="godfellas">B</md-option>
							<md-option value="pulp_fiction">C</md-option>
							<md-option value="scarface">D</md-option>
						</md-select>
					</md-input-container>

					<md-input-container>
						<label>Stream</label>
						<md-input required></md-input>
					</md-input-container>

					<md-input-container md-inline>
						<label>Specialization</label>
						<md-input required></md-input>
					</md-input-container>

					<md-input-container>
						<label>Sub-specialization</label>
						<md-input required type="number"></md-input>
					</md-input-container>
				</form>
			</md-step>
			<md-step md-label="STEP 2" md-message="Personal Information">
				<form novalidate @submit.stop.prevent="submit">

					<md-input-container>
						<label>Date of birth</label>
						<md-input type="number"></md-input>
					</md-input-container>

					<md-input-container>
						<label for="movie">Gender</label>
						<md-select name="movie" id="movie">
							<md-option value="fight_club">Male</md-option>
							<md-option value="godfather">Female</md-option>
							<md-option value="godfather_ii">Transgender</md-option>
						</md-select>
					</md-input-container>

					<md-input-container>
						<label for="movie">Category</label>
						<md-select name="movie" id="movie">
							<md-option value="fight_club">General</md-option>
							<md-option value="godfather">SC</md-option>
							<md-option value="godfather_ii">ST</md-option>
							<md-option value="godfather_iii">OBC</md-option>
							<md-option value="godfellas">PH</md-option>
						</md-select>
					</md-input-container>

					<md-input-container>
						<label for="movie">Marital Status</label>
						<md-select name="movie" id="movie">
							<md-option value="fight_club">Married</md-option>
							<md-option value="godfather">Unmarried</md-option>
						</md-select>
					</md-input-container>

					<md-input-container>
						<label for="movie">Nationality</label>
						<md-select name="movie" id="movie">
							<md-option value="fight_club">Indian</md-option>
							<md-option value="godfather">NRI</md-option>
						</md-select>
					</md-input-container>

					<md-input-container>
						<md-icon>phone</md-icon>
						<label>Phone</label>
						<md-input type="tel"></md-input>
					</md-input-container>

					<md-input-container>
						<md-icon>speaker_notes</md-icon>
						<label>E-Mail</label>
						<md-textarea></md-textarea>
					</md-input-container>

					<md-input-container>
						<label>Address</label>
						<md-textarea maxlength="70"></md-textarea>
					</md-input-container>

				</form>
			</md-step>
			<md-step md-label="STEP 3" md-message="Experience">

			</md-step>
			<md-step md-label="STEP 4" md-message="Education">
				<p>This seems something I need to focus on just after the first step.</p>
			</md-step>
			<md-step md-label="STEP 5" md-message="Publications">
				<p>This seems something I need to focus on just after the first step.</p>
			</md-step>
			<md-step md-label="STEP 6" md-message="Conferences/Seminars/Workshops">
				<p>This seems something I need to focus on just after the first step.</p>
			</md-step>
			<md-step md-label="STEP 7" md-message="Research Projects">
				<p>This seems something I need to focus on just after the first step.</p>
			</md-step>
			<md-step md-label="STEP 8" md-message="Other Information">
				<div align="left">
				<span class="md-display-1">Please select any of the following that may apply to you: </span><br><br>
				<md-checkbox id="my-test7" name="my-test7" class="md-primary">Has there been any break in your academic career? </md-checkbox><br>
				<md-checkbox id="my-test7" name="my-test7" class="md-primary">Have you been punished during your studies at College/University?</md-checkbox><br>
				<md-checkbox id="my-test7" name="my-test7" class="md-primary">Were you at any time declared medically unfit or asked to submit your resignation or dismissed?</md-checkbox><br>
				<md-checkbox id="my-test7" name="my-test7" class="md-primary">Do you have any court case pending as one of the parties?</md-checkbox><br>
				<md-checkbox id="my-test7" name="my-test7" class="md-primary">Have you undergone any selection process with Manipal University Jaipur or Manipal Group Institutions previously?</md-checkbox><br>
				</div>
			</md-step>
		</md-stepper>

		<md-speed-dial md-open="hover" class="md-fab-bottom-left">
			<md-button class="md-fab" md-fab-trigger>
				<md-icon md-icon-morph>close</md-icon>
				<md-icon>share</md-icon>
			</md-button>

			<md-button class="md-fab md-primary md-mini md-clean">
				<md-icon>email</md-icon>
			</md-button>

			<md-button class="md-fab md-primary md-mini md-clean">
				<md-icon>content_copy</md-icon>
			</md-button>
		</md-speed-dial>

	</div>
</template>

<script>
	import Hello from './components/Hello'

	export default {
		name: 'app',
		data() {
			return {
				initialValue: 'John/Jane Doe'
			};
		},

		methods: {
			toggleLeftSidenav() {
				this.$refs.leftSidenav.toggle();
			},
			toggleRightSidenav() {
				this.$refs.rightSidenav.toggle();
			},
			closeRightSidenav() {
				this.$refs.rightSidenav.close();
			},
			open(ref) {
				console.log('Opened: ' + ref);
			},
			close(ref) {
				console.log('Closed: ' + ref);
			},
			fetchFunction(param) {
				// param = { queryParam: query }

				// 'fetchAutocomplete' should return a Promise.

				// md-autocomplete will call fetchAutocomplete and pass
				// 'param' as an argument.
				// the 'param' is composed by a query param and
				// a query.
			}
		}
	}

</script>

<style>
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
	}

</style>
