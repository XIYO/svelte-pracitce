<h1>translateZ 테스트</h1>

<h2>translateZ의 움직임 기준이 어떻게 되는건지 명확히 확인한다.</h2>

<div id="observer">
	<div id="x">
		mouse hover x
		<div> hi</div>
	</div>
	<div id="y">
		mouse hover y
		<div>
			hi
		</div>
	</div>
	<div id="z">
		mouse hover z
		<div style="height: 100px; width: 100px; display: flex; justify-content: center; align-items: center">
			hi
		</div>
	</div>
</div>

<style>
    #observer {
        /*perspective: 500px;*/

				* {
						transition: all 1s;
				}
    }

    #x:hover > div {
        transform: translateX(200px);
        background-color: lightcoral;
    }

    #y:hover > div {
        transform: translateY(200px);
        background-color: lightgreen;
    }

		#z {
        perspective: 500px;

				background-color: cornflowerblue;

				display: inline-block;
				&> div {
						transform-origin: center;
						background-color: green;
        }

				&:hover {
						background-color: coral;
            transform: translateZ(100px);
				}
		}

    #z:hover > div {
        transform: translateZ(100px);

        background-color: mediumpurple;
    }
</style>