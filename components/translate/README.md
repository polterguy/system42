
Translate component
===============

This folder contains Active Events that allows you to translate a piece of text, from one source language, to any destination language you
wish. Notice that this component uses Google Translate, which means that your text is passed on to Google. Which might pose provacy risks
for you.

The Active Event is called **[sys42.translate]** and takes the source text as **[_arg]**, in addition to a **[src-lang]** and
a **[dest-lang]** argument. Below is an example of translating a piece of English text into Japanese.

```
sys42.translate:Hello, my name is Thomas Hansen
  src-lang:en
  dest-lang:ja
```

The **[src-lang]** is optional, and will be automatically determined if possible.
