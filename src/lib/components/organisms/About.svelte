<script>
	import SparklingHighlight from '$lib/components/molecules/SparklingHighlight.svelte';
	import Socials from '$lib/components/molecules/Socials.svelte';
	import Image from '../atoms/Image.svelte';
</script>

<section
	id="about"
	style="max-width: 600px; margin: 0 auto; grid-template-columns: auto; place-content: center;
  text-align: center;"
>
	<div class="info">
		<h2>
			Водата е богатство,
			<SparklingHighlight color="secondary">водата е живот!</SparklingHighlight>
		</h2>
		<p>
			Ако познаваме, ако пазим, ако се грижим за богатата дунавска екосистема с хиляди видове
			растения, животни и микроорганизми ползите ще бъдат дългосрочни.
		</p>
	</div>
	<!-- <div class="image">
		<Image src="/images/danube.jpg" alt="Image of the Danube river" />
	</div> -->
</section>

<style lang="scss">
	@import '$lib/scss/breakpoints.scss';

	#about {
		position: relative;
		display: grid;
		grid-template-columns: 500px 250px;
		align-items: center;
		justify-content: space-between;
		padding-bottom: 50px;

		@include for-phone-only {
			grid-template-columns: 1fr;
			justify-items: center;
			gap: 20px;
		}

		.info {
			display: flex;
			flex-direction: column;
			gap: 10px;
			h2 {
				@include for-phone-only {
					text-align: center;
				}
			}

			p {
				@include for-phone-only {
					text-align: justify;
				}
			}

			@include for-phone-only {
				gap: 20px;
			}
		}

		.socials {
			display: flex;
			align-items: center;
			gap: 15px;

			@include for-phone-only {
				justify-content: center;
				margin-bottom: 10px;
				span {
					display: none;
				}
			}
		}

		.image {
			width: 420px;
			height: 420px;
		}
	}
</style>
