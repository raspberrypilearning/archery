## निशाना लगाने वाला तीर

चलो शुरू करते हैं बनाने एक तीर जो स्क्रीन के चारों ओर घूमता है।

\--- task \---

स्क्रैच स्टार्टर प्रोजेक्ट खोलें।

**ऑनलाइन**: स्टार्टर प्रोजेक्ट को [rpf.io/archeryon](http://rpf.io/archeryon){: target = "_ blank"} पर खोलें।

यदि आपके पास एक स्क्रैच खाता है, तो आप ** रीमिक्स ** पर क्लिक करके कापी बना सकते हैं ।

**ऑफलाइन**:खोलो[ स्टार्टर प्रोजेक्ट](http://rpf.io/p/en/archery-go){:target="_blank"} को ऑफलाइन एडिटर में खोलिये।

यदि आपको स्क्रैच ऑफ़लाइन एडिटर को डाउनलोड और इंस्टॉल करने की आवश्यकता है, तो आप इसे [rpf.io/scratchoff](http://rpf.io/scratchoff) {:target="_blank"} पर पा सकते हैं।

स्टार्टर प्रोजेक्ट में, आपको एक लक्ष्य पृष्ठभूमि और एक क्रॉस हेयर स्प्राइट देखना चाहिए।

![प्रारंभक प्रोजैक्ट](images/archery-starter.png)

\--- /task \---

\--- task \---

जब आपका खेल शुरू होता है, एक नया तीर शूट करने के लिए एक संदेश प्रसारित करें।

![लक्ष्य स्प्राइट](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Once this message has been received, set the arrow's position and size.

![लक्ष्य स्प्राइट](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Click the green flag to test your game. You should see your arrow get bigger and move to the bottom-left of the stage.

![larger target sprite in bottom left of stage](images/archery-start-test.png)

\--- /task \---

\--- task \---

Add code to your arrow so that it `glides`{:class="block3motion"} randomly around the stage `forever`{:class="block3control"}.

![target sprite](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

\--- /task \---

\--- task \---

Test your game again, and you should see your arrow move randomly around the stage.

![target in a different position](images/archery-glide-test.png)

\--- /task \---