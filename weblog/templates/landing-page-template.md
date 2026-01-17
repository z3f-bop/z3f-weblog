Type: Template
Title: Landing Page Template

<!DOCTYPE html>
<html lang="en">
<head>
<title>{weblog-title}</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
{feeds}
<style>
@import url('https://static.omg.lol/type/font-honey.css');
@import url('https://static.omg.lol/type/font-lato-regular.css');
@import url('https://static.omg.lol/type/font-lato-bold.css');
@import url('https://static.omg.lol/type/font-lato-italic.css');
@import url('https://static.omg.lol/type/font-md-io.css');
@import url('https://static.omg.lol/type/fontawesome-free/css/all.css');

:root {
	--foreground: #212529;
	--background: transparent;
	--link: #0b7285;
	--accent: #6b7280;
	--purple: #9775fa;
	--card-bg: rgba(255, 255, 255, 0.5);
}

@media (prefers-color-scheme: dark) {
	:root {
		--foreground: #eee;
		--background: transparent;
		--link: #67e8f9;
		--accent: #9ca3af;
		--purple: #c4b5fd;
		--card-bg: rgba(0, 0, 0, 0.5);
	}
}

* { box-sizing: border-box; }

body {
	font-family: 'Lato', sans-serif;
	font-size: 120%;
	color: var(--foreground);
	background: linear-gradient(135deg, #c084fc 0%, #a78bfa 25%, #7dd3fc 75%, #22d3ee 100%);
	background-attachment: fixed;
	min-height: 100vh;
}

h1, h2, h3, h4, h5, h6 {
	font-family: 'VC Honey Deck', serif;
	margin: 1rem 0;
}

p, li { line-height: 160%; }

.container {
	max-width: 50em;
	margin: 3em auto;
	padding: 2em 2.5em;
	background: var(--card-bg);
	border-radius: 1.5em;
	backdrop-filter: blur(10px);
	box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

header, main, footer {
	max-width: 100%;
	margin: 0;
	padding: 0;
}

header { margin-bottom: 1.5em; }

footer p {
	margin-top: 5em;
	font-size: 90%;
	text-align: center;
}

a:link, a:visited, a:hover, a:active { color: var(--link); }

.header-content {
	display: flex;
	align-items: center;
	gap: 1.25em;
}

.pfp {
	width: 96px;
	height: 96px;
	border-radius: 1em;
	object-fit: cover;
	box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
	flex-shrink: 0;
}

.header-text {
	flex: 1;
	min-width: 0;
}

.weblog-title {
	margin-top: 0;
}

.weblog-title a {
	text-decoration: none;
	color: var(--foreground);
}

.weblog-description {
	font-size: 90%;
	color: var(--accent);
	margin-top: -0.5em;
}

article {
	margin: 3em 0;
	padding-bottom: 2em;
	border-bottom: 1px solid var(--accent);
}

article h2 a {
	text-decoration: none;
	color: var(--foreground);
}

article h2 a:hover {
	color: var(--link);
}

.post-meta {
	font-size: 85%;
	color: var(--accent);
}

.read-more {
	margin-top: 1em;
}

.read-more a {
	color: var(--purple);
	text-decoration: none;
}

.read-more a:hover {
	text-decoration: underline;
}

hr {
	border: 0;
	height: 1px;
	background: var(--accent);
	margin: 2em 0;
}

code {
	padding: .2em .3em;
	border: 1px solid var(--accent);
	font-family: 'MD IO 0.4';
	font-size: 90%;
}

pre code {
	background: #000;
	color: #eee;
	display: inline-block;
	padding: 1em;
	white-space: pre-wrap;
}

img { max-width: 100%; }

.tag {
	background: var(--accent);
	color: var(--background) !important;
	padding: .3em .4em;
	margin: .8em 0 0 .4em;
	border-radius: .5em;
	text-decoration: none;
	display: inline-block;
	font-size: 85%;
}
</style>
</head>
<body>

<div class="container">
	<header>
		<div class="header-content">
			<a href="https://z3f.omg.lol"><img src="https://profiles.cache.lol/z3f/picture" alt="z3f" class="pfp"></a>
			<div class="header-text">
				<h1 class="weblog-title"><a href="{base-path}">{weblog-title}</a></h1>
				<p class="weblog-description">{weblog-description}</p>
			</div>
		</div>
		{navigation}
	</header>

	<main>
		<h2>Recent Posts</h2>
		{post-list}
	</main>

	<footer>
		<p>Made with <a href="https://weblog.lol">weblog.lol</a> · 💜</p>
	</footer>
</div>

</body>
</html>
