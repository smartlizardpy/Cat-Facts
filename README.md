# Cat-Facts
This is a app made with Tkinter and Httplib2.This app was built using [Cat Facts API]([https://pages.github.com/](https://catfact.ninja/)https://catfact.ninja/).
- 
You can use this snippet with the proper imports
```
import json
import httplib2
```
```
h = httplib2.Http()
resp, content = h.request("https://catfact.ninja/fact")
x = content
y = json.loads(x)
quote = y["fact"]

    T.delete(1.0, END)  # Clear the current text in the Text widget
    T.insert(END, quote)  # Insert the new quote into the Text widget

```

