<h1>You look wonderful!</h1>
<div class="gallery">
    <div class="row">
        <div class="column">
            <img src="assets/gallery/zagboon.png" alt="Zag Boon" style="width:100%">
            <img src="assets/gallery/zagxmas.png" alt="Zag Xmas" style="width:100%">
            <img src="assets/gallery/meg.png" alt="Meg" style="width:100%">
            <img src="assets/gallery/kit.png" alt="Kit" style="width:100%">
        </div>
        <div class="column">
            <img src="assets/gallery/zag.png" alt="Zag" style="width:100%">
            <img src="assets/gallery/charon.png" alt="Charon" style="width:100%">
            <img src="assets/gallery/hermes.png" alt="Hermes" style="width:100%">
            <img src="assets/gallery/merrymaker.png" alt="Merry-Maker" style="width:100%">
        </div>
    </div>
</div>

<style>
    .row{
        display: flex;
        flex-wrap: wrap;
        padding: 0 7px;
        margin: auto;
    }

    .column{
        flex: 50%;
        max-width: 48%;
        padding: 0 5px;
    }

    .column img {
        margin-top: 10px;
        vertical-align: middle;
        width: 100%;
    }

    h1{
        text-align: center;
        font-weight: lighter;
        color: rgb(255, 255, 255);
    }

    .gallery{
        border-radius: 10px;
        max-height: 86%;
        width: 85%;
        display: block;
        margin: auto;
        padding: 20px;
        background-color: #7c0000;
        overflow-y: scroll;
    }

    @media screen and (max-width: 800px) {
    .column {
        flex: 45%;
        max-width: 50%;
    }
    }

    @media screen and (max-width: 600px) {
    .column {
        flex: 100%;
        max-width: 100%;
    }
}
</style>