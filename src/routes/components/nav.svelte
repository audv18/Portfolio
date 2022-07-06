<nav>
    <div class= "main">
        <header>
            <input type="checkbox" name="" id="">
            <a href="/">Home</a> |
            <a href="/about">About</a> | 
            <a href="/work">Work</a> |
            <a href="mailto:danielsuandrew@gmail.com">Contact</a>
        </header>
    </div>
</nav>

<style>
    .main {
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    header{
        position: relative;
        width: 70px;
        height: 25px;
    }
    header input{
        position: absolute;
        width: 100%;
        height: 100%;
        cursor: pointer;
        z-index: 5;
        -webkit-appearance: none;
        outline: none;
    }
    header input::before{
        content: '\f0c9';
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        color: white;
    }
    header input:checked::before{
        content: '\f00d';
    }
    header a{
        position: absolute;
        opacity: 0;
        transform: translate(0);
        color: rgb(20, 35, 108);
    }
    header a:hover{
        color: rgb(7,32,255)
    }
    header input:checked ~ a{
        display: block;
        opacity: 1;
    }
    header input:checked ~ a:nth-child(2){
        transform: translate(-200px);
    }
    header input:checked ~ a:nth-child(3){
        transform: translate(-100px);
    }
    header input:checked ~ a:nth-child(4){
        transform: translate(100px);
    }
    header input:checked ~ a:nth-child(5){
        transform: translate(210px);
    }
    a {
        color:rgb(20, 35, 108);
        text-decoration: none;
    }
    a:hover {
        color: rgb(7, 32, 255);
    }
</style>

