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
</body>

<div class="copyright-wrap">
    <Copyright/>
</div>

<style>
     body {
        background: #384143;
        color:white;
        font-family: 'Raleway', sans-serif;
        padding: 10px;
    }
    .layoutdiv {
        max-width: 90%;
        margin: auto;
    }
.copyright-wrap {
   bottom: 0px;
   text-align: center;
   position: fixed;
   width: 100%;
}
</style>
