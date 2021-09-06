<head>
	<link rel="stylesheet" href="path/to/font-awesome/css/font-awesome.min.css" />
</head>
<div class="w-full py-12 px-4 sm:px-6 lg:py-16 lg:px-8 z-20">
	<h1 class="text-3xl font-extrabold text-black dark:text-white sm:text-4xl">
		<span class="block"> This is Energify. </span>
	</h1>
	<p class="text-md mt-4 text-gray-400">
		A web application designed to save money, as well as the environment.
	</p>
</div>
<h2 class="text-3xl font-extrabold text-black dark:text-white sm:text-4xl">
	<span class="block"> Our Mission </span>
</h2>
<br />
<br />
<div class="row">
	<div class="column">
		<div class="card">
			<h3>Reduce Wastage</h3>
			<p>
				When using fossil fuels, more than 60% of energy used for electricity generation is lost in
				conversion. This amount of wastage is detrimental to the planet.
			</p>
			<p>
				Yet by switching to renewable energy sources with Energify, you can up to half this wastage!
			</p>
		</div>
	</div>

	<div class="column">
		<div class="card">
			<h3>Save Money</h3>

			<p>
				As much as you may not want to admit it, people are selfish creatures at heart, and saving
				money is exactly the thing which will prompt people to do more for the planet.
			</p>
			<p>
				Sound like a plan? Energify helps you start saving right away thanks to on-demand expert
				help
			</p>
		</div>
	</div>

	<div class="column">
		<div class="card">
			<h3>Conserve Resources</h3>
			<p>
				Fossil fuels are a finite resource and we are consuming them at a rate at which they cannot
				be prouduced fast enough to satisfy our ever-growing needs.
			</p>
			<p>Soon enough, we will run out.</p>
			<p>Save fossil fuels and help the planet with Energify by your side!</p>
		</div>
	</div>

	<div class="column">
		<div class="card">
			<h3>Protect the Planet</h3>
			<p>
				We are the very last generation which can prevent irreversible damage to the planet as a
				result of climate change.
			</p>
			<p>
				Do your part. Don't sit back and wait for others to do it for you. If we all work together,
				we CAN combat climate change.
			</p>
		</div>
	</div>
</div>
<br />
<br />
<br />
<h2 class="text-3xl font-extrabold text-black dark:text-white sm:text-4xl">
	<span class="block"> Our Creators </span>
</h2>
<br />
<br />
<div class="row2">
	<div class="column2" style="background-color:#aaa;">
		<img
			src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/user_photos/001/630/688/datas/profile.jpg"
		/>
		<h2>Sebastian Ponce</h2>
		<p>
			I'm Sebastian, a Data Science student who applies data to solve real-world problems and
			creates solutions using ML models.
		</p>
	</div>
	<div class="column2" style="background-color:#bbb;">
		<img src="https://avatars.githubusercontent.com/u/67038775?height=180&v=4&width=180" />
		<h2>Juan Almanza</h2>
		<p>14 yo. Baby (I don't get to Jr) fullstack dev. studying DS, AI and ML.</p>
	</div>
	<div class="column2" style="background-color:#ccc;">
		<img
			src="https://yt3.ggpht.com/ejo_AdogqdFzFPXgphGC0k1Q3jAsXucqCD042mgYSdjkI7EdsStCqWJVBDC_oKuqC1OdTnMdUg=s88-c-k-c0x00ffffff-no-rj-mo"
		/>
		<h2>Erin McGurk</h2>
		<p>
			Avid web and app developer who enjoys using React Native and MERN stack to create innovative
			and exciting new applications. Hopes to become the next Elon Musk :)
		</p>
	</div>
	<div class="column2" style="background-color:#ddd;">
		<img src="" />
		<h2>Zhuo en Chua</h2>
		<p>
			Enthusiastic programmer and pitch extrodinaire! Enjoys machine learning and discovering the
			wonders of Quantum Computing
		</p>
	</div>
</div>

<style>
	* {
		box-sizing: border-box;
	}

	h2 {
		text-align: center;
	}

	h3 {
		font-size: 25px;
		font-weight: bold;
		color: green;
	}

	/* Float four columns side by side */
	.column {
		float: left;
		width: 25%;
		padding: 0 10px;
	}

	/* Remove extra left and right margins, due to padding */
	.row {
		margin: 0 -5px;
	}

	/* Clear floats after the columns */
	.row:after {
		content: '';
		display: table;
		clear: both;
	}

	/* Responsive columns */
	@media screen and (max-width: 600px) {
		.column {
			width: 100%;
			display: block;
			margin-bottom: 20px;
		}
	}

	/* Style the counter cards */
	.card {
		box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
		padding: 16px;
		text-align: center;
		background-color: #fff;
		border-radius: 30px;
	}

	.column2 {
		float: left;
		width: 25%;
		padding: 10px;
		height: 300px; /* Should be removed. Only for demonstration */
	}

	/* Clear floats after the columns */
	.row2:after {
		content: '';
		display: table;
		clear: both;
	}

	img {
		height: 90px;
		width: 90px;
		border-radius: 50%;
		display: block;
		margin-left: auto;
		margin-right: auto;
	}
</style>
