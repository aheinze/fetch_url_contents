# fetch_url_contents

fetch_url_contents - a simple js to php proxy function to get cross domain content.

### Requirements

- Browser needs to support Promises


### Get started

Include fuc.js.php

```<script src="fuc.js.php"></script>```

You can now get cross domain content via the global ```fetch_url_contents(url [, type])``` function.

### Usage

Get just the content as text

```js
fetch_url_contents(url).then(function(content){

  console.log(content);
  
}).catch(function(){

  alert('Request failed!');

});
```

Query the content

```js
fetch_url_contents(url, 'html').then(function(dom){

  console.log(dom.querySelectorAll('img')); // get all images
  
}).catch(function(){

  alert('Request failed!');

});
```

Get JSON

```js
fetch_url_contents(url, 'json').then(function(json){

  console.log(json);
  
}).catch(function(){

  alert('Request failed!');

});
```
