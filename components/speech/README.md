
Speech component
===============

This folder contains a couple of helper Active Events that will use speech synthesis to speak some given text, in whatever language you wish
to have it speak in. Notice, which languages is supported, depends upon your browser's installed languages.

It contains two Active Events.

- **[sys42.speak]** Speaks the given text
- **[sys42.speak.query]** Queries the supported languages and voices

Notice, the **[sys42.speak.query]** Active Event, requires a client-side roundtrip, to query your browser for its supported languages.
Hence, you will have to supply a lambda callback when invoking it, which will be invoked with its supported voices when it has determined
the supported voices. An example of an invocation to this event is given below.

```
sys42.speak.query
  .on-finished
    sys42.windows.show-lambda:x:/..
```

Which will result in something resembling the following.

```
.on-finished
  voices
    Alex:en-US
      local:true
    Alice:it-IT
      local:true

    /* ...snip ...*/

    Google 普通话（中国大陆）:zh-CN
      local:false
    Google 粤語（香港）:zh-HK
      local:false
    Google 國語（臺灣）:zh-TW
      local:false
  sys42.windows.show-lambda:x:/..
```

Notice the **[local]** argument for each voice, which is important in regards to understanding privacy, since if local is false, it means
that it is not a locally installed voice generator, but in fact an external service.

To speak something in English for instance, you could use something like the following. Assuming you have English installed as one of your
supported languages.

```
sys42.speak:Hello World, my name is Marvin!
  voice:en-US
```

The above will use the first available "en-US" voice, if any. If you wish to use an explicit voice instead, you could use something 
like the following, assuming you have "Samantha" installed.

```
sys42.speak:Hello World, my name is Samantha!
  voice:Samantha,en-US
```



