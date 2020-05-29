## तीर चलाना

जब स्पेस बार दबाया जाता है तो शूट करने के लिए अपने तीर को कोड करें।

\--- task \---

जब स्पेस बार दबाया जाता है तो दूसरी script (एक तीर चलाना) बंद करें। 

![निशाना sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

अपने प्रोजैक्ट का फिर से जाँच करें। इस समय, आपका तीर चलना बंद कर देना चाहिए **जब स्पेस बार दबाया जाता है।**

\--- /task \---

\--- task \---

अपने तीर को चेतन करें, ताकि ऐसा लगे कि यह लक्ष्य की ओर बढ़ रहा है।

![लक्ष्य sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

अपने खेल का फिर से परीक्षण करें। इस बार, जब आप स्पेस बार दबाते हैं, तो आपको अपने तीर को छोटा होना चाहिए, जैसे कि वह लक्ष्य की ओर बढ़ रहा हो।

![target with the cross hair on it](images/archery-animate-test.png)

\--- /task \---

\--- task \---

एक बार जब आपका तीर निशाने पर होगा, तो आप खिलाड़ी को बता सकते हैं कि उन्होंने कितने अंक बनाए हैं। For example, they could score 200 points for hitting the yellow.

![target sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
+if <touching color (#ffff00) ?> then
say [200 points] for (2) seconds
end
```

\--- /task \---

\--- task \---

You can also play a sound if they hit the yellow.

![target sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
+start sound (cheer v)
say [200 points] for (2) seconds
end
```

\--- /task \---

\--- task \---

Finally, you need to broadcast the `new arrow`{:class="block3events"} message again to get a new arrow.

![target sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
start sound (cheer v)
say [200 points] for (2) seconds
end
+broadcast (new arrow v)
```

\--- /task \---