<template>
	<div class="left">
		<header>
			<img
				alt="Vue logo"
				src="https://i.pinimg.com/474x/a8/fd/a7/a8fda7c27257787b4b7e948c2e9e4e57.jpg"
				height="200"
			/>

			<p v-if="seen">Now you see me</p>

			<h2>Hola, soy {{ nombre }}</h2>
			me apellido

			<h4>
				{{ apellido }}
			</h4>

			y soy de

			<h1>
				{{ edad >= 18 ? 'Puedes Votar' : 'No Puedes Votar' }}
			</h1>

			<h2>
				{{ edad }}
			</h2>

			<a @click="handleClick">Saludo!</a>

			<br />

			<select v-model="selecte">
				<option disabled value="">Seleciona un deporte</option>
				<option>Futbol</option>
				<option>Baloncesto</option>
				<option>Tenis de mesa</option>
				<option>Futsal</option>
			</select>

			<br />

			<span>De mis deportes favoritos: {{ selecte }}</span>

			<br />

			<select v-model="selected">
				<option v-for="option in options" v-bind:value="option.value" :key="option.id">
					{{ option.text }}
				</option>
			</select>
			<br />
			<span>Seleccionado: {{ selected }}</span>
		</header>
	</div>
</template>

<script>
export default {
	methods: {
		handleClick: function() {
			alert('Hola Williams')
		},
	},

	props: ['tipomascota', 'nombre', 'apellido'],

	data() {
		return {
			variable1: 'valorvariable',

			mensaje1: 'hola',

			mensaje: 'Soy UGB',

			mensaje2: 'hoy es',

			mensaje3: 'martes 06 de abril',

			name: '',

			picked: '',

			precio: 24,

			edad: 12,

			seen: false,

			selecte: '',

			selected: 'A',
			options: [
				{ text: 'Uno', value: 'A' },
				{ text: 'Dos', value: 'B' },
				{ text: 'Tres', value: 'C' },
			],
		}
	},
}
</script>

<style scoped>
body {
	width: 100%;

	max-width: 68rem;

	margin: 0 auto;

	font: 1.6rem/1.25 'Helvetica Neue', Helvetica, Arial, sans-serif;

	background-color: #f5f5f5;

	color: #4d4d4d;

	-moz-osx-font-smoothing: grayscale;

	-webkit-font-smoothing: antialiased;
}

h2 {
	color: #40078aad;

	text-align: center;

	font-weight: bold;
}

h4 {
	color: rgb(185, 8, 162);

	text-align: center;
}

h1 {
	color: #f5716c;

	text-align: center;

	font-weight: bold;
}

.left {
	width: 40%;

	position: fixed;

	display: flex;

	justify-content: center;

	align-items: center;

	height: 79vh;

	margin-left: 350px;
}
</style>
