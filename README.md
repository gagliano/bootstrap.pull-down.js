Bootstrap Pull down event
=========================

Implementing pullDown event by jQuery with bootstrap style. 
PullDown is most used to refresh page by touch(drag), move down and drop finger from display.


<img src="preview.jpg" alt="Preview" />

## Version 0.1.2


insert this lines to your app:

<pre>
&lt;!DOCTYPE html>
&lt;html>
	&lt;head>
		&lt;meta charset="utf-8" />
		&lt;meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=0" />
		&lt;link href="bootstrap.pull-down.css" rel="stylesheet" media="screen">
		&lt;link href="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.3.1/css/bootstrap-combined.min.css" rel="stylesheet">
		&lt;script src="http://code.jquery.com/jquery-1.9.1.min.js">&lt;/script>
		&lt;script src="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.3.1/js/bootstrap.min.js">&lt;/script>
		&lt;script src="bootstrap.pull-down.js">&lt;/script>
		&lt;script type="text/javascript">
			$(document).ready(function () {
				$.pullDown.start();
			});
		&lt;/script>
	&lt;/head>
	&lt;body>
		&lt;div class="pull-down">
			&lt;a href="#" class="work">&lt;i class="indicator-click icon-refresh icon-large">&lt;/i>&lt;/a>
			&lt;i class="indicator icon-down-arrow icon-large">&lt;/i>
			&lt;i class="indicator-working icon-roundabout icon-large">&lt;/i>
			&lt;span class="pulled-label">Uvolněním aktualizovat&lt;/span>
			&lt;span class="pull-label">Stažením aktualizovat&lt;/span>
			&lt;span class="default-label">Kliknutím aktualizovat&lt;/span>
			&lt;span class="working-label">Aktualizuji&lt;/span>
			&lt;button type="button" class="close stop">&lt;i class="icon-large icon-remove-2">&lt;/i>&lt;/button>
		&lt;/div>
		&lt;div style="height: 300px;" class="hero-unit">
			Some text of page
		&lt;/div>
	&lt;/body>
&lt;/html>
</pre>


API-documentation
-----------------

### Events:

<code>pullDown</code>
	- if pulled down (time to refresh)
	
<code>pullDownStopWorking</code>
	- if clicked to stop refreshing


-----------------------------------------------------------------
### Options:

<code>container</code>
	- which element react to touches

<code>pullDown</code>
	- the element contained the pullDown pane at top


-----------------------------------------------------------------
### Methods:

<code>start(options)</code>
	- start the pullDown

<code>enable()</code>
	- set as enabled and start (default is enabled)

<code>disable()</code>
	- set as disabled and start (refresh pane isstatic)

<code>loading(status)</code>
	- show loading spinner if status true or hide if status false (like pulled down event trigged)


-----------------------------------------------------------------
### Properties:

<code>container</code>
	- the global container element for pullDown

<code>element</code>
	- the pullDown element
