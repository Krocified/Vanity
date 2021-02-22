<script>
    let bgImage = "assets/zag.png"
</script>

<div id="header" style="background-image: url({bgImage})">
	<h1>
		Vanity
    </h1>
    <p>
        Your Daily Source of Self Esteem
    </p>
</div>
<div id="announcement">
    <h4>
        Don't forget to sleep!
    </h4>
</div>

<style>
    
    #header{
        margin-top: 0;
		background-color: #ec4646;
        background-size: cover;
		width: 100%;
		height: 40vh;
    }

    #announcement{
        margin-top: 0;
		background-color: #222222;
		width: 100%;
		height: 75px;
    }

    h1{
        margin: 0;
        padding-top: 15vh;
        color: white;
        font-size: 10vw;
        text-transform: uppercase;
        text-align: center;
    }

    h4{
        margin: 0;
        padding-top: 15px;
        color: white;
        font-size: 5vw;
        text-align: center;
        font-weight: lighter;
    }

    p{
        margin: 0;
        color: white;
        font-size: 5vw;
        font-weight: lighter;
        text-align: center;
    }

    @media (min-width: 700px) {
        #announcement{
            height: 75px;
        }      
        #header{
            height: 425px;
        } 
		h1 {
            padding-top: 225px;
            margin-left: 15%;
            font-size: 70px;
			text-align: left;
        }

        h4{
            font-size: 30px;
        }

        p {
            margin-left: 15%;
            font-size: 30px;
			text-align: left;
        }
	}
</style>