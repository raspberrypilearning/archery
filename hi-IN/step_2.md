## निशाना लगाने वाला तीर

चलो शुरू करते हैं बनाने एक तीर जो स्क्रीन के चारों ओर घूमता है।

--- task ---

स्क्रैच स्टार्टर प्रोजेक्ट खोलें।

**ऑनलाइन**: स्टार्टर प्रोजेक्ट को [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"} पर खोलें।

यदि आपके पास एक स्क्रैच खाता है, तो आप **रीमिक्स** पर क्लिक करके कापी बना सकते हैं ।

**ऑफलाइन**:खोलो[ स्टार्टर प्रोजेक्ट](https://rpf.io/p/hi-IN/archery-go){:target="_blank"} को ऑफलाइन एडिटर में खोलिये।

यदि आपको स्क्रैच ऑफ़लाइन एडिटर को डाउनलोड और इंस्टॉल करने की आवश्यकता है, तो आप इसे [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"} पर पा सकते हैं।

स्टार्टर प्रोजेक्ट में, आपको एक लक्ष्य पृष्ठभूमि और एक क्रॉस हेयर स्प्राइट देखना चाहिए।

![प्रारंभक प्रोजैक्ट](images/archery-starter.png)

--- /task ---

--- task ---

जब आपका खेल शुरू होता है, एक नया तीर शूट करने के लिए एक संदेश प्रसारित करें।

![लक्ष्य स्प्राइट](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

--- /task ---

--- task ---

यह संदेश प्राप्त होने के बाद, तीर की स्थिति और आकार सेट करें।

![लक्ष्य स्प्राइट](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

अपने खेल का परीक्षण करने के लिए हरे झंडे पर क्लिक करें। आपको अपने तीर को बड़ा होता हुआ देखना चाहिए और चरण के नीचे-बाएँ चलना चाहिए।

![बड़े लक्ष्य स्प्राइट मंच के नीचे बाईं ओर](images/archery-start-test.png)

--- /task ---

--- task ---

अपने बाण पर कोड जोड़ें ताकि यह `glide`{:class="block3motion"} निरुद्देश्यता से स्टेज `forever`{:class="block3control"}।

![लक्ष्य स्प्राइट](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

अपने खेल का फिर से परीक्षण करें, और आपको अपने तीर को मंच के चारों ओर बेतरतीब ढंग से घूमते हुए देखना चाहिए।

![एक अलग स्थिति में लक्ष्य](images/archery-glide-test.png)

--- /task ---
