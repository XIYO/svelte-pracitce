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
	:global(#practice-002) {
			background-color: darkorange;
			view-transition-name: practice-002;
  }

  @keyframes fade-in {
      from { opacity: 0; }
  }

  @keyframes fade-out {
      to { opacity: 0; }
  }

  @keyframes slide-from-right {
      from { transform: translateX(30px); }
  }

  @keyframes slide-to-left {
      to { transform: translateX(-30px); }
  }

  :root::view-transition-old(practice-002) {
      animation: 90ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
      300ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
  }

  :root::view-transition-new(practice-002) {
      animation: 210ms cubic-bezier(0, 0, 0.2, 1) 90ms both fade-in,
      300ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
  }
</style>