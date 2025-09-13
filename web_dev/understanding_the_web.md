---
title: Understanding the Web
nav_order: 4
has_children: false
parent: Web Development
layout: page
header-includes:
- \pagenumbering{gobble}
---

### Introduction
Before we start writing HTML or CSS, let’s try to understand **what actually happens when you type “www.google.com” in your browser**  

If you think the answer is simply “the page loads”… well, you’re technically right, but let’s peek under the hood. Knowing what’s happening makes you a better web developer.  

### The Client–Server Model
The web typically relies on this model for everything. a client requests something, the server provides it or doesn't provide based on availability of the requested item.
Think of it like this:  
- **you (the client)** open a browser, **the server** is like a restaurant kitchen.
- You place an order (“GET me google.com”), the server prepares the meal (the HTML, CSS, JavaScript).  
- The waiter (the network) brings it back to your table (your browser).  

If the kitchen is slow or the waiter gets lost, you wait longer. If the order doesn’t exist, the waiter comes back saying, *“404 — we don’t have that.”*  

### What’s inside a URL?
- A Uniform Resource Locator (URL) is what we mostly call "link" casually. It is what is used to identify an item on the internet, just like how your name, index number and maybe programme is used to identify you on the KNUST campus by anyone.
- a URL has to be unique(never be the same as another). That is why it is made up of a couple of id items put together as one.
- Take this example:  
`https://www.example.com:443/home?search=cat#section`  

let's break it down:  
- `https://` → The protocol that the web works on, mentioned below. this is actually a variant of it (a more secure one).  
- `www.example.com` → The restaurant’s address (domain name).  
- `:443` → The door number (port).  
- `/home` → Which part of the menu you want.  
- `?search=cat` → Special instructions (like “extra cheese”).  
- `#section` → Where on the page you want to jump to.  

Now, you will not see the port numbers in most URLs, but they are all necessary, just discretely handled by the networking component, but this should explain the concept of URLs clear enough.

### HTTP
The web speaks a language called **HTTP** (HyperText Transfer Protocol) and it is the only language it understands, just like Asante Twi is only language **all** Ashantis understand. Every request you make and every response the server gives follows this protocol.  
A request is simply your URL, so the examples are countless, but the responses that the server can give are classified into few classes.
Some common responses are:  
- **200 OK** → “Here’s your page, all good.”  
- **301 Moved Permanently** → “We’ve changed the address; go there instead.”  
- **404 Not Found** → “Oops, that page doesn’t exist.”  
- **500 Internal Server Error** → “The kitchen exploded. Try later.”  

### how your browser renders a page
all browsers render pages the same way, and it simply detailed below;
1. Browser requests the HTML.  
2. HTML comes back and says, “I also need these CSS and JS files.”  
3. Browser fetches them.  
4. Browser builds the page piece by piece until you see it.  

That’s why sometimes pages load text first and then images “pop in” later.  But essentially all of this is done very fast.

### why should you care about all these as a beginner?
Because soon, when your own projects don’t work, you’ll need to open **DevTools** in your browser to figure out whether the problem is:  
- your HTML,  
- your CSS/JS, or  
- something broken in the client-server conversation.  


### Assignment
1. Do the “Inspect → Network tab” exercise and write down the first 3 requests you see (and their status codes).  
2. Using your words, explain what happens between the time you press enter on a URL and when the page loads. (Keep it simple — no essays needed.)  

---
