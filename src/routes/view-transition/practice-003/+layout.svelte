<ul>
	<li>
		<a href="a">a</a>
	</li>
	<li>
		<a href="b">b</a>
	</li>
	<li>
		<a href="c">c</a>
	</li>
</ul>

<div>
	<span>
	  <slot />
	</span>
</div>

<style>
    div {
        border: 1px solid black;
        perspective: 500px;

				span {
						display: block;
						background-color: lightblue;
						transition: transform 1s;
						transform-style: preserve-3d;
						transform-origin: center;
				}

        &:hover {

            span {
                transform: translateZ(250px) rotateY(560deg);
                background-color: coral;
            }

            &::after {
                content: '💬💬💬💬';
            }
        }

        &::before, &::after {
            content: '🎮🎮🎮🎮';
        }
    }

    :global(#practice-003) {
        background-color: cadetblue;
        view-transition-name: practice-003;
    }

    :global(main::before, main::after) {
        content: '🎈🎈🎈🎈';
    }

    :root::view-transition {
        perspective: 500px;
        border: 10px solid blue;
    }

    :root::view-transition-group(practice-003),
    :root::view-transition-image-pair(practice-003) {
        transform-style: preserve-3d;
        isolation: auto;
    }

    :root::view-transition-old(practice-003),
    :root::view-transition-new(practice-003) {
        mix-blend-mode: normal;
        backface-visibility: hidden;
    }

    :root::view-transition-group(practice-003) {
        animation: 300ms ease forwards zoom-out, 300ms ease 950ms forwards zoom-in;
        border: 5px solid mediumpurple;
    }

    :root::view-transition-old(practice-003),
    :root::view-transition-new(practice-003) {
        animation: ease 400ms forwards flip-out;
        border: 5px solid red;
    }

    :root::view-transition-new(practice-003) {
        animation-name: flip-in;
        transform: rotateY(180deg);
        border: 5px solid green;
    }

    @keyframes zoom-out {
        0% {
            transform: translateZ(0);
        }
        100% {
            transform: translateZ(-600px);
        }
    }

    @keyframes zoom-in {
        0% {
            transform: translateZ(-600px);
        }
        100% {
            transform: translateZ(0);
        }
    }

    @keyframes flip-out {
        0% {
            transform: rotateY(0);
        }
        100% {
            transform: rotateY(-180deg);
        }
    }

    @keyframes flip-in {
        0% {
            transform: rotateY(180deg);
        }
        100% {
            transform: rotateY(0deg);
        }
    }

</style>