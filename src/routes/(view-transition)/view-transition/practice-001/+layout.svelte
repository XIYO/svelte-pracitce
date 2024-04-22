<ul>
	<li>
		<a href="a">a</a>
	</li>
	<li>
		<a href="b">b</a>
	</li>
</ul>
<slot />

<style>
    :root::view-transition-group(box) {
        /*border-image: url('/octagon.svg') 33% / 30px / 30px;*/
        /*overflow: clip;*/
        /*animation: heightClose 0.5s,  1s heightOpen 0.5s ;*/
        /*animation: ua 0.5s;*/
        animation-delay: 0.25s;
        animation-duration: 0.25s;
    }

    :root::view-transition-image-pair(box) {
        border-image: url('/octagon.svg') 33% / 30px;
        animation: 0.25s shutter forwards, 0.25s shutter 0.5s reverse forwards;
        overflow: clip;
        /*border: palevioletred 10px solid;*/
    }

    :root::view-transition-old(box) {
        border-image: url('/octagon.svg') 33% / 30px;
        /*animation: 5s hide 0.5s forwards;*/
        animation: 0.25s ehide 0.25s forwards;
        /*animation: 0.25s hide 1s;*/
        /*border: palevioletred 10px solid;*/
        /*object-fit: none;*/
        /*display: none;*/
    }

    :root::view-transition-new(box) {
        border-image: url('/octagon.svg') 33% / 30px;
        /*display: none;*/
        /*animation: none;*/
        /*animation: 10s show 0.5s forwards;*/
        opacity: 0;
        animation: 0.25s eshow 0.25s forwards;

        /*height: 100%;*/
        /*border: palevioletred 10px solid;*/
        /*object-fit: none;*/
    }

    @keyframes shutter {
        from {
            height: 100%;
        }
        to {
            height: 0;
        }
    }

    @keyframes ehide {
        50% {
            opacity: 1;
        }
        51% {
            opacity: 0;
        }
        100% {
            opacity: 0;
        }
    }

    @keyframes eshow {
        50% {
            opacity: 0;
        }
        51% {
            opacity: 1;
        }
        100% {
            opacity: 1;
        }
    }
</style>