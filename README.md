# Example-code

This repo shows how to make a webpage title change between different words/messages.

-Full step-by-step guide is in [Guide.txt](./Guide.txt).  
-Or just look at the example code below:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Changing Title</title>
  <script>
    const titles = ["Hello", "Welcome", "HI", "Blop!"];
    let index = 0;
    setInterval(() => {
      document.title = titles[index];
      index = (index + 1) % titles.length;
    }, 1000);
  </script>
</head>
</html>
