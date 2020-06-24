## तीर चलाना

जब स्पेस बार दबाया जाता है तो शूट करने के लिए अपने तीर को कोड करें।

--- task ---

जब स्पेस बार दबाया जाता है तो दूसरी script (एक तीर चलाना) बंद करें। 

![निशाना sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

अपने प्रोजैक्ट का फिर से जाँच करें। इस समय, आपका तीर चलना बंद कर देना चाहिए **when the space bar is pressed**

--- /task ---

--- task ---

अपने तीर को चेतन करें, ताकि ऐसा लगे कि यह लक्ष्य की ओर बढ़ रहा है।

![लक्ष्य sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

--- /task ---

--- task ---

अपने खेल का फिर से परीक्षण करें। इस बार, जब आप स्पेस बार दबाते हैं, तो आपको अपने तीर को छोटा होना चाहिए, जैसे कि वह लक्ष्य की ओर बढ़ रहा हो।

![लक्ष्य के साथ बाल पार करना](images/archery-animate-test.png)

--- /task ---

--- task ---

एक बार जब आपका तीर निशाने पर होगा, तो आप खिलाड़ी को बता सकते हैं कि उन्होंने कितने अंक बनाए हैं। उदाहरण के लिए, वे पीले मारने के लिए 200 अंक बना सकते थे।

![निशाना sprite](images/target-sprite.png)

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

--- /task ---

--- task ---

यदि आप पीले रंग से टकराते हैं तो आप ध्वनि भी बजा सकते हैं।

![लक्ष्य sprite](images/target-sprite.png)

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

--- /task ---

--- task ---

अंत में, आपको एक नया तीर प्राप्त करने के लिए `new arrow`{:class="block3events"} संदेश को फिर से ब्राडकास्ट करने की आवश्यकता है।

![लक्ष्य sprite](images/target-sprite.png)

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

--- /task ---