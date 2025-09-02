how to make the title to change between different words/messages??? :D

1.Make a list of titles, for example like this (const titles = ["Hello", "Welcome", "HI", "Blop!"];)

2.now we need to keep track of which one we’re showing, for example like this (let index = 0;) 
index is like a pointer At the start, it’s 0, meaning we show the first item ("Hello")

3. after that we need to change the title every second, for example like this (setInterval(() => {...}, 1000);)
setInterval Run the code inside every 1000 milliseconds (1 second)

4. after that setInterval we need to Set the page title inside the {...} , for example like this (document.title = titles[index];)
This replaces the text on the browser tab with the current item in the list

now the result of what you did should be like this:

const titles = ["Hello", "Welcome", "HI", "Blop!"];
     let index = 0;
    setInterval(() => {
      document.title = titles[index];}, 1000);


5. now that you've done that we need to do this one (Move to the next word) below the (document.title = titles[index];) , for example (index = (index + 1) % titles.length;)
index + 1 moves to the next position
% titles.length makes sure we loop back to 0 when we reach the end

now it's done ! ! !, make sure your result is like this 

const titles = ["Hello", "Welcome", "HI", "Blop!"];
     let index = 0;
    setInterval(() => {
      document.title = titles[index];
      index = (index + 1) % titles.length;
    }, 1000);
