<script>
    let name = 'Glen Chan-Choong'

    // component imports
    import Button from '$lib/Button/Button.svelte';
	import IconButton from '$lib/IconButton/IconButton.svelte';

    // icons import
    // @ts-ignore
    import IoLogoInstagram from 'svelte-icons/io/IoLogoInstagram.svelte'
	// @ts-ignore
    import IoLogoLinkedin from 'svelte-icons/io/IoLogoLinkedin.svelte'
	// @ts-ignore
    import IoIosMail from 'svelte-icons/io/IoIosMail.svelte'

</script>

<div class="grid">
	<div class="text">
		<p>{name}</p>

        <Button text="Enter" link="/work"/>

        <div class="iconButtonWrapper">
            <IconButton link="https://www.instagram.com/glenchanchoong/">
                <IoLogoLinkedin/>
            </IconButton>

            <IconButton link="https://www.instagram.com/hakka.designs/">
                <IoLogoInstagram/>
            </IconButton>

            <IconButton link="https://www.instagram.com/glenchanchoong/">
                <IoIosMail/>
            </IconButton>
        </div>
	</div>

	<div class="image">
		<img
			alt="donut and coffee place"
			src="https://cdn.myportfolio.com/7bf13fc8-be3c-4bd4-96b0-ae0f57e2689c/5b23af0c-ec60-4c9a-84a6-d873664e0e9b_rwc_0x0x1783x1179x4096.png?h=a702da7ab03e39908a66c52e6fc85ef6"
		/>
	</div>
</div>

<style>
    /* font import */
    @import url(https://db.onlinewebfonts.com/c/facc2325c1dff1377bb6bf9f0fb965f6?family=Museo+Slab+W00+900);

    .iconButtonWrapper{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 15px;
    }

	.grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		width: 100%;
		justify-items: center;
		align-items: center;
        overflow: hidden;
	}

	.grid > div {
		width: 100%;
		height: 100%;
	}

	.text {
		display: flex;
        flex-direction: column;
		text-align: center;
		justify-content: center;
		align-items: center;
        gap: 30px;
	}

    p{
        font-weight: 900;
        font-size: 69px;
        margin:0;
        font-family: "Museo Slab W00 900";
        color:#444444
    }

	.image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	/* when grid is smaller than 600px */
	@media only screen and (max-width: 600px) {
		.grid {
			grid-template-columns: 1fr;
			/* reverse put title on bottom*/
		}
	}
</style>
