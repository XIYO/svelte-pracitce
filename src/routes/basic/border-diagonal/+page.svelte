<script>
</script>

<h1>보더 사선 만들기</h1>

<h2>type 1</h2>
<div>content</div>

<h2>type 2</h2>
<div>content</div>

<h2>type 3</h2>
<div>
	<svg width="200" height="100">
		<line x1="0" y1="100" x2="200" y2="0" stroke="black" stroke-width="2" />
	</svg>
</div>

<h2>type 4</h2>
<div>content</div>

<h2>type 5</h2>
<div>content</div>

<h2>type 6</h2>
<div>content</div>
<button>dynamicsize</button>


<style>
    div {
        width: 100px;
        height: 100px;
        border: 5px solid black;
    }

    /** 보더가 아님 컨텐츠에 배경을 칠함 */
    div:nth-of-type(1) {
        border-top: 5px solid red;
        border-right: 5px solid blue;
        border-bottom: 5px solid green;
        border-left: 5px solid yellow;
        height: 100px;
        background: linear-gradient(45deg, transparent 50%, black 50%);

    }

    /** 해킹 기법 */
    div:nth-of-type(2) {
        width: 0;
        height: 0;
        border: unset;
        border-top: 50px solid transparent;
        border-right: 50px solid red;
    }

    div:nth-of-type(3) {
        border: 5px solid red;
        border-top-color: blue;
        border-right-color: green;
        border-bottom-color: yellow;
    }

    div:nth-of-type(4) {
        border: unset;
        background-color: blue;
        padding: 20px;
        transform: skewX(-20deg);
    }

    div:nth-of-type(5) {
        width: 250px;
        height: 250px;
        background-color: coral;
        border: 32px solid;
        border-image: url(https://skullctf.com/images/skull-border.svg) 32 round;
    }

		div:nth-of-type(6) {
				color: lemonchiffon;
				width: 250px;
				height: 250px;
				/*background-color: cornflowerblue;*/
				background-clip: padding-box;
				border-width: 90px;
				border-image-source: url(/octagon.svg);
				border-image-slice: 33% fill;
				border-image-repeat: repeat;
		}
</style>