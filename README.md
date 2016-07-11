<!--Theme101-->
<!--First Theme for Tumblr for practice.-->

<!DOCTYPE html>
<html>
<head>
<!--Meta not working-->
<meta charset="utf-8">
    <title>{block:TagPage}{Tag} | {/block:TagPage} {block:SearchPage}{lang:Search results for SearchQuery} | {/block:SearchPage}{block:PostSummary}{PostSummary} | {/block:PostSummary}{Title}</title>
    {block:Description}
    <meta name="description" content="{MetaDescription}" />
    {/block:Description}

    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="shortcut icon" href="{Favicon}"/>
    <link rel="alternate" type="application/rss+xml" href="{RSS}"/>
    <link rel="apple-touch-icon-precomposed" href="{PortraitURL-128}">

    <link rel="stylesheet" href="http://static.tumblr.com/xeccbfq/9Qenv9yn8/normalize.min.css" />
    <link rel="stylesheet" href="http://static.tumblr.com/xeccbfq/lT5nwa5y4/theme.css" />

<title>{Title}</title>
<style>

      /* TODO: JS: Grid layout from Chapter 4 */

      /* TODO: JS: loading message from Chapter 4 */

      /* TODO: Tumblr: Add CSS customization from Chapter 3 */


  header {
    background: url(http://dash.ga.co/assets/gene-bg.png);
  }
  header a {
    text-decoration: none;
    color: #fff;
  }
  h1 {
    display: inline;
    position: absolute;
    top: 60px;
    font-size: 42px;
    color: #fff;
  }
  h2 {
    display: inline;
    color: #fff;
    position: absolute;
    top: 120px;
    font-size: 20px;
  }
  body {
    background: #eee;
    font-family: sans-serif;
  }
  .post {
    background: #fff;
    margin: 40px auto;
    padding: 20px;
    border-radius: 6px;
    width: 640px;
  }
  .avatar {
    margin: 60px 30px;
    border-radius: 100%;
  }
  .container {
    width: 640px;
    margin: 0 auto;
  }
  .like-reblog {
    list-style: none;
    border: 1px solid #ccc;
    }
    .like-reblog li {
      float: right;
      padding: 6px;
      height: 20px;
    }
</style>
</head>

<body>
  <header>
  <div class="container">
    <img class="avatar" src="{PortraitURL-128}">
    <h1><a href="{BlogURL}">{Title}</a></h1>
    {block:Description}
      <h2>{Description}</h2>
    {/block:Description}
  </div>
  </header>
  
	{block:Posts}
		{block:Text}
		<div class="post">
			{block:Title}
				<h3>
					<a href="{Permalink}">{Title}</a>
				</h3>
			{/block:Title}
			{Body}
			<ul class="like-reblog">
			  <li>{LikeButton}</li> 
			  <li>{ReblogButton}</li>
			  <li>{block:NoteCount}{NoteCountWithLabel}{/block:NoteCount}</li>
		  </ul>
		</div>
		{/block:Text}

		{block:Photo} 
		<div class="post">	
			<img src="{PhotoURL-500}">
			{block:Caption}{Caption}{/block:Caption}
			<ul class="like-reblog">
			  <li>{LikeButton}</li> 
			  <li>{ReblogButton}</li>
			  <li>{block:NoteCount}{NoteCountWithLabel}{/block:NoteCount}</li>
		  </ul>
		</div>
		{/block:Photo}

		{block:Quote}
		<div class="post">
			{Quote}
	   	{block:Source}<br>&mdash;{Source}{/block:Source}
	   	<ul class="like-reblog">
			  <li>{LikeButton}</li> 
			  <li>{ReblogButton}</li>
			  <li>{block:NoteCount}{NoteCountWithLabel}{/block:NoteCount}</li>
		  </ul>
		</div>
		{/block:Quote}

		{block:Link}
		<div class="post">
  			<a href="{URL}" {Target}>{Name}</a>
  			{block:Description}{Description}{/block:Description}
  			<ul class="like-reblog">
			  <li>{LikeButton}</li> 
			  <li>{ReblogButton}</li>
			  <li>{block:NoteCount}{NoteCountWithLabel}{/block:NoteCount}</li>
		  </ul>
  		</div>
		{/block:Link}

		{block:Chat}
		<div class="post">
			<h3>{block:Title}{Title}{/block:Title}</h3>
			<table>
				{block:Lines}
				<tr>
					<th>{block:Label}{Label}{/block:Label}</th>
					<td>{Line}</td>
				</tr>
				{/block:Lines}
			</table>
			<ul class="like-reblog">
			  <li>{LikeButton}</li> 
			  <li>{ReblogButton}</li>
			  <li>{block:NoteCount}{NoteCountWithLabel}{/block:NoteCount}</li>
		  </ul>
		</div>
		{/block:Chat}
	
		{block:Audio}
		<div class="post">
			{AudioPlayer}
      	{block:Caption}{Caption}{/block:Caption}
      	<ul class="like-reblog">
			  <li>{LikeButton}</li> 
			  <li>{ReblogButton}</li>
			  <li>{block:NoteCount}{NoteCountWithLabel}{/block:NoteCount}</li>
		  </ul>
		</div>
		{/block:Audio}

		{block:Video}
		<div class="post">
			{Video-500}
			{block:Caption}{Caption}{/block:Caption}
			<ul class="like-reblog">
			  <li>{LikeButton}</li> 
			  <li>{ReblogButton}</li>
			  <li>{block:NoteCount}{NoteCountWithLabel}{/block:NoteCount}</li>
		  </ul>
		</div>
		{/block:Video}

    
    
	{/block:Posts}
</body>
</html>
