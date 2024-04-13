<ul>
	<li>
		<a href="a">A</a>
	</li>
	<li>
		<a href="b">B</a>
	</li>
	<li>
		<a href="c">C</a>
	</li>
</ul>

<slot />

<style>
	:global(#practice-003) {
			background-color: cadetblue;
			view-transition-name: practice-003;
  }

  :root::view-transition {
      perspective: 1000px;
      background: mediumpurple;
      inset: 0;
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

  :root::view-transition-group(practice-003) {
      animation: 300ms ease forwards zoom-out, 300ms ease 950ms forwards zoom-in;
      /*animation: 300ms ease forwards zoom-out;*/
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
</style>