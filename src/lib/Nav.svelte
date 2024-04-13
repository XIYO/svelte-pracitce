<nav>
	<ul>
		<li>
			<a href="/">Home</a>
		</li>
		<li>
			<a href="/view-transition">View transition</a>
			<ul>
				<li>
					<a href="/view-transition/practice-001">practice-001</a>
				</li>
				<li>
					<a href="/view-transition/practice-002">practice-002</a>
				</li>
				<li>
					<a href="/view-transition/practice-003">practice-003</a>
				</li>
			</ul>
		</li>
	</ul>
</nav>

<style>
		:global(body) {
				margin-inline-end: 20rem;
		}
    nav {
        position: fixed;
        inset-block: 0;
        inset-inline-end: 0;
        width: 20rem;

        background: cornflowerblue;
        color: lemonchiffon;

        font-weight: bold;
        font-size: 2rem;

        a {
            color: unset;
        }

        view-transition-name: nav;
    }
</style>