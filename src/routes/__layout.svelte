<script>
    import Nav from "./components/nav.svelte";
    import Copyright from "./components/copyright.svelte";
</script>

<svelte:head>
    <link rel="stylesheet" href="./routes/app.css">
</svelte:head>

<body>
    <div class="layoutdiv">
        <Nav/>
        <slot/>
    </div>
    <div class="copyright-wrap">
        <Copyright/>
    </div>
</body>

<style>
     body {
        background:black;
        color:white;
        font-family: 'Raleway', sans-serif;
        padding: 10px;
    }

    .layoutdiv {
        max-width: 90%;
        margin: auto;
    }
.copyright-wrap {
   position: absolute;
   bottom: 0px;
   margin: auto;
}
</style>
