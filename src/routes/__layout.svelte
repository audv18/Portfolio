<script>
    import Nav from "./components/nav.svelte";
    import Copyright from "./components/copyright.svelte";
import PageTransition from "./components/PageTransition.svelte";
    export let url;
</script>

<svelte:head>
    <link rel="stylesheet" href="./routes/app.css">
</svelte:head>

<body>
    <div>
        <div class="layoutdiv">
            <Nav/>
        </div>
        <div class="maintext">
            <PageTransition { url }>
                <slot/>
            </PageTransition>
        </div>
    </div>
</body>

<div class="copyright-wrap">
    <Copyright/>
</div>

<style>
    .maintext {
        text-align: justify;
        text-justify: inter-word;
    }
     body {
        background: #fffbec;
        color:rgb(20, 35, 108);
        font-family: 'Raleway', sans-serif;
        padding: 10px;
        text-align: justify;
        text-justify: inter-word;
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

<script context="module">
/**@type {import('sveltejs/kit').Load}*/
export const load = async ({ url }) => ({ props: { url }});
</script>





