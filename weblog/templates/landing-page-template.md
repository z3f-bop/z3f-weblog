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
	--background: #f8f9fa;
	--link: #0b7285;
	--accent: #868e96;
	--purple: #9775fa;
}

@media (prefers-color-scheme: dark) {
	:root {
		--foreground: #eee;
		--background: #222;
		--link: #99e9f2;
		--accent: #ced4da;
		--purple: #b197fc;
	}
}

* { box-sizing: border-box; }

body {
	font-family: 'Lato', sans-serif;
	font-size: 120%;
	color: var(--foreground);
	background: var(--background);
}

h1, h2, h3, h4, h5, h6 {
	font-family: 'VC Honey Deck', serif;
	margin: 1rem 0;
}

p, li { line-height: 160%; }

header, main, footer {
	max-width: 60em;
	margin: 2em auto;
	padding: 0 1em;
}

header { margin-top: 4em; }

footer p {
	margin-top: 5em;
	font-size: 90%;
	text-align: center;
}

a:link, a:visited, a:hover, a:active { color: var(--link); }

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

<header>
	<h1 class="weblog-title"><a href="{base-path}">{weblog-title}</a></h1>
	<p class="weblog-description">{weblog-description}</p>
	{navigation}
</header>

<main>
<h2>Recent Posts</h2>
{post-list}
</main>

<footer>
	<p>Made with <a href="https://weblog.lol">weblog.lol</a> · 💜</p>
</footer>

</body>
</html>
