<h3>What?</h3>
<p>A jQuery plugin to assist with handling the file drag and drop api being implemented with HTML 5.</p>

<h3>Usage</h3>

<p>You can use the following line to deactivate undesired drop zones, by preventing the default browser actions
and preventing files from being dropped.</p>
<pre>
    <code>$('div.nodrop').fileDragDrop({dropEffect: false});</code>
</pre>

<p>Next, we can initialize a desired drop zone for all of the events; dragover, dragleave, and drop.</p>
<pre>
    <code>$('div.dropzone').fileDragDrop();</code>
</pre>

<p>A callback should almost immediately be added in order to notify the user or perform an action. We have to add the method as well.</p>
<pre>
    <code>$('div.dropzone').fileDragDrop('init', {}, function(){
    	alert('file(s) dropped!');
    });</code>
</pre>

<p>You can also segregate the events individually.</p>
<pre>
    <code>$('div.dropzone').fileDragDrop('init', {types: ['dragover']}, function(evt){
    	alert('file(s) drug over!');
    });</code>
</pre>

<p>The 'handleFiles' method can be used to attach the dropped file(s) object to a dom object via the jQuery data function.</p>
<pre>
    <code>$('div.dropzone').fileDragDrop('handleFiles', {attach: true, evt: e}, function(e){
    	alert('file(s) attached to the drop zone!');
    });</code>
</pre>

<h3>Help?</h3>
<p>This is my first jQuery plugin and I welcome any and all help to make it leaner, cleaner, and more efficient.</p>