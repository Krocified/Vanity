<script>
    let name = ""
    let email = ""
    let message = ""

    function alert(){
        alert("A mortal called "+name+" from "+email+" wants to tell you that \'"+message+"\'.")
    }
</script>

<div class="contact">
    <img src="assets/hermes.png" alt="Hermes">
    <div class="form">
        <h1>
            Do you have a message for Olympus?
        </h1>
        <form class="forminput" action="">
            <input type="text" placeholder="Your Name" id="name">
            <input type="text" placeholder="Your Email" id="email">
            <textarea name="message" id="message" cols="30" rows="5" placeholder="Your Message"></textarea>
            <input type="submit" on:click="{alert}">
        </form>
        <button on:click="{alert}">SUBMIT</button>
    </div>
</div>

<style>
    .contact{
        height: 500px;
        background-color: hsl(23, 90%, 54%);
        position: relative;
    }

    img{
        position: absolute;
        bottom: 0;
        height: 450px;
        left: -100px;
    }

    .form{
        float: right;
        width: 55%;
    }

    .forminput{
        max-width: 850px;
        margin: auto;
        display: flex;
        flex-direction: column;
    }

    input[type=text]{
        width: 50vw;
        margin: auto;
        margin-bottom: 20px;
        padding: 15px;
    }

    input[type=submit]{
        width: 30%;
        padding: 20px;
        margin: auto;
        margin-top: 20px;
        border-radius: 5px;
        background-color: hsl(23, 90%, 40%);
        border: 0px;
        color: white;
        text-transform: uppercase;
        display: none;
    }

    button{
        width: 30%;
        padding: 20px;
        margin: auto;
        margin-top: 20px;
        border-radius: 5px;
        background-color: hsl(23, 90%, 40%);
        border: 0px;
        color: white;
    }

    textarea {
        width: 50vw;
        margin: auto;
        padding: 15px;
    }

    h1{
        text-align: center;
        font-weight: lighter;
        margin: 3%;
        color: hsl(0, 0%, 0%);
    }

    @media (max-width: 850px) {
		.contact{
            height: 1000px;
            margin-top: 1000px;
            bottom: 0;
        }

        .form{
            width: 100%;
        }

        input[type=text]{
            width: 90vw;
            margin: auto;
            margin-bottom: 20px;
            padding: 15px;
        }

        textarea {
            width: 90vw;
            margin: auto;
            padding: 15px;
        }
	}
</style>