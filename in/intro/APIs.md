# WWW: World Wide Web (...and python!)

In this lecture, we will be discussing how computers safely interact with one another and how we can leverage python to do the same.

## HTTP: Hyper Text Transfer Protocol

This is basically a series of rules that are put in place to "communicate" over the internet. At the end of the day, this is all just text messages that are flowing back and forth from one computer to another.

**In short, we use HTTP to request data from other machines which we can then use for fun or profit**.

## Clients and Servers

The **client** is the machine that is making a request to some other computer for information. For example, when we visit google.com, we are the **client** requesting data from a machine that has the data we want.

The machine that processes our request is called the **server**, which is typically a computer that lives in a server farm somewhere. It runs a highly specialized software that is built to process and respond to millions of such requests per minute.

![1](https://dzone.com/storage/temp/3794445-dig-2.png)

## Requests and Responses

In HTTP parlance, we have the "request" and the 'response". A request is what a client makes to the server. The server can respond back with a variety of different messages.

Both requests and responses are formulated in a specific manner, usually it looks like this:

![2](https://dpsvdv74uwwos.cloudfront.net/statics/img/drive/70so2pl_1isfech3j3uy0iow_upjs5twpwu.jpeg)

### Key terms

* **path** or **endpoint** or most generally, **url**: the location on the internet we want to make the request to
* **headers**: meta information about the request, stuff like browser name (User-Agent, etc)
* **body**: the information to send in request or recieve in response

### Header types

Headers can be grouped as follows although this is more of a trivia question than anything else.

![3](https://mdn.mozillademos.org/files/13821/HTTP_Request_Headers2.png)

### Sample Response

![4](https://1.bp.blogspot.com/-TaY2IVbMnlc/V6m0B9LUMRI/AAAAAAAAAgc/2bqzdMOVkcgwG9fG-5uDIJ7VmMLW1EJ9gCEw/s1600/http_response.png)

Generally, speaking:

![4](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/1046558602/original/requestpacket-body.jpg?1477975936)

## HTML: Hyper Text Markup Language

This is simply a language encoding that browsers understand. Based on the definition of these encodings, we can generate interactive web sites like the ones we have seen thus far.
