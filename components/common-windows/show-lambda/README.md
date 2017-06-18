
Debugging your apps, by inspecting your lambda objects
========

This folder creates a small debug helper window, that displays whatever lambda object you wish to display. Example of usage
can be found below.

```
_foo
  bar:Howdy
sys42.windows.show-lambda:x:/..
```

The above would look like the following.

![alt tag](screenshots/example-ajax-debug-hyperlambda-window-screenshot.png)

Arguments;

* [_arg] - And expression leading to whatever lambda you want to see.
* [class] - CSS class to display your window with. Defaults to "col-xs-12 show-code-window".
* [parent] - Which parent to inject your window into. Defaults to "content".

To see only parts of your stack, you can pass in an expression, leading to the part you wish to see. Example below.

```
_foo
  bar:Howdy
sys42.windows.show-lambda:x:/../*/_foo
```

Due to the nature of Hyperlambda, being an input/output language, changing as you execute parts of it - This window is actually highly
useful, for watching parts of your code, at the point you invoke your window. If you don't know what a piece of code looks like, at some
specific point in your execution, then this is easy to see, by invoking the show-lambda window, at the point in your code, where
you wish to inspect its code.

You can create multiple windows of this type during one request. The last window you create, will be shown above the previous window you created.
