# LocalStorage

> [!INFO] What is local storage?
> You can think of local storage as a place that your browser stores small pieces of information about you, locally.
> It is typically used to store small pieces of information, like your user preferences (whether you are using dark mode or not 😈), and IDs.

#### Local storage stores data in the form of key - value pairs. You can think of this like a name tag associated with each value. Whenever you are trying to look for something, all you need to know is the name tag!

> [!ERROR] But what are some of the issues of this?
>
> - Anybody can manipulate local storage. Cannot store any sensitive information.
> - Size limitation - Can only store 5MB.
> - Possiblity of leaking sensitive information.
> - [Cross site scripting attacks](https://shahjerry33.medium.com/xss-the-localstorage-robbery-d5fbf353c6b0)

> [!SUCCESS] Tasks.
>
> 1. Your task is to exploit the local storage on the website.
> 2. Firstly, how do you navigate to where you can view local storage? (Hint: Right click!)
> 3. Then, what can you do with the data that is being stored there. What format is it in? Can you modify it?
