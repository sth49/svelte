<script>
	import Header from "./Header.svelte";
	import RadioCheck from "./RadioCheck.svelte";
</script>
<title>My Scatterplot</title>
<body>
	<Header/>
	<main class='container'>
		<div class="row pt-2">
			<div class='col-1 pe-2 text-end'>
				<strong>X:</strong>
			</div>
			<div class='col-11'>
				<RadioCheck checked=true value='SepalLength' id='x-sl' />
				<RadioCheck value='SepalWidth' id='x-sw'/>
				<RadioCheck value='PetalLength' id='x-pl'/>
				<RadioCheck value='PetalWidth' id='x-pw'/>
			</div>
		</div>
		<div class="row">
			<div class='col-1 pe-2 text-end'>
				<strong>Y:</strong>
			</div>
			<div class='col-11'>
				<RadioCheck checked=true name='y-encoding' value='SepalLength' id='y-sl' />
				<RadioCheck name='y-encoding' value='SepalWidth' id='y-sw'/>
				<RadioCheck name='y-encoding' value='PetalLength' id='y-pl'/>
				<RadioCheck name='y-encoding' value='PetalWidth' id='y-pw'/>
			</div>
		</div>
		<div class="row">
			<div class="col">
				<div class="form-check form-switch">
					<input class="form-check-input" type="checkbox" role="switch" id="use-color"/>
					<label class="form-check-label" for="use-color">Color-encode Class</label>
				</div>
			</div>
		</div>
		<div class="text-end">
			<button class="btn btn-primary">Update</button>
			<button class="btn btn-secondary">Reset</button>
		</div>
		<div class="text-center">
			<svg width="400" height="400">
				<circle cx="300" cy="300" r="5" fill="red"></circle>
				<circle cx="250" cy="100" r="5" fill="blue"></circle>
				<circle cx="150" cy="200" r="5" fill="green"></circle>
				<line x1="30" x2="380" y1="350" y2="350" stroke="black" stroke-width="1"></line>
				<line x1="30" x2="30" y1="20" y2="350" stroke="black" stroke-width="1"></line>
				<text x="380" y="355" text-anchor="end" alignment-baseline="hanging">SepalLength</text>
				<text x="-100" y="20" transform="rotate(-90)" alignment-baseline="baseline">SepalWidth</text>
			</svg>
		</div>
	</main>
</body>


<style>
	body {
        background: #eee;
    }
	.container{
		width: 640px;
		background-color: white;
	}
</style>