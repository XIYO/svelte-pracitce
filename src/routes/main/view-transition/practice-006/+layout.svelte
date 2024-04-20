<script></script>

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

<slot />

<style>
    @keyframes heightAnimation {
        0%, 100% {
            /*height: 100%;  !* 시작 및 종료 높이 *!*/
        }
        50% {
            height: 0; /* 중간 높이 */
        }
    }

    @keyframes hide {
        0% {
            opacity: 1;

        }
        100% {
            opacity: 0;
        }
    }

		@keyframes show {
				0% {
						opacity: 0;

				}
				100% {
						opacity: 1;
				}
		}

    :root::view-transition-group(practice-006) {
        /*animation: hide 1s;*/

    }

    :root::view-transition-old(practice-006) {
        display: none;
				/*animation: hide 1s;*/
				height: 100%;
				/*overflow: clip;*/
				/*object-fit: cover;*/
    }

    :root::view-transition-new(practice-006) {
				animation: none;
        /*animation: show 1s 2s;*/
        height: 100%;
        /*object-fit: none;*/
        /*border-image: url('/octagon.svg') 33% fill / 30px / 30px round;*/
        /*border: 1rem solid darkmagenta;*/
        contain: content;
        overflow: clip;
				/*object-fit: cover;*/
    }

    :root::view-transition-group(practice-006) {
				/*border: 1rem solid darkmagenta;*/
        /*border-image: url('/skull-border.svg') 33% / 30px;*/
				/*overflow: clip;*/

        border-image: url('/octagon-red.svg') 33% / 30px;
        /*border-image: url(/skull-border.svg) 32 / 32px round;*/
				/*border-image-source: url(/skull-border.svg);*/

				background-color: cornflowerblue;
				overflow: clip;
				z-index: 100;
    }

    :root::view-transition-image-pair(practice-006) {
        border-image: url('/skull-border.svg') 33% / 30px;
				overflow: clip;
				background-color: yellowgreen;
				z-index: 55;
    }
</style>
