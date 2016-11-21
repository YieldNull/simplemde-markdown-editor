# Customize

I **don't** wanna editor to be rendered.

So I changed mode `gfm` to `text/plain`

```javascript
mode.name = "text/plain";
```

And I want to insert the image url to editor after uploading it.

So I added a function `insertImage(url)`, according to `drawImage()`;

```javascript
SimpleMDE.prototype.insertImage = function(url) {
	//drawImage();
	var cm = this.codemirror;
	var stat = getState(cm);
	var options = this.options;

	_replaceSelection(cm, stat.image, options.insertTexts.image, url);
};
```
