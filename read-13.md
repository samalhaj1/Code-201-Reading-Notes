# HTML5 Browser Storage: the Past, Present and Future

## Why Store Data on the Client?
The main reason is practicality. JavaScript code running on the browser does not necessarily need to send all information to the server. There are several use cases:

* You want to increase performance. You can cache data client-side so it can be retrieved without additional server requests.

* You have a significant quantity of client-side-only data, e.g. HTML strings or widget configuration settings.

* You want make your application work off-line.

![img](https://clementbuchanan.github.io/reading-notes/images/html5.jpg)

**DIVING IN**

Persistent local storage is one of the areas where native client applications have held an advantage over web applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files, or some other place according to platform convention. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions.

Historically, web applications have had none of these luxuries. Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:

1. Cookies are included with every 

HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over

2. Cookies are included with every 

HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over  SSL)

3. Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful

What we really want is 

* a lot of storage space on the client

* that persists beyond a page refresh

* and isn’t transmitted to the server

Before  HTML5, all attempts to achieve this were ultimately unsatisfactory in different ways.

## INTRODUCING HTML5 STORAGE

What I will refer to as “ HTML5 Storage” is a specification named Web Storage, which was at one time part of the  HTML5specification proper, but was split out into its own specification for uninteresting political reasons. Certain browser vendors also refer to it as “Local Storage” or “ DOM Storage.” The naming situation is made even more complicated by some related, similarly-named, emerging standards

From your JavaScript code, you’ll access  HTML5 Storage through the localStorage object on the global window object. Before you can use it, you should detect whether the browser supports it.

 **check for  HTML5 Storage**

    function supports_html5_storage() 
    try {
    return 'localStorage' in window && window['localStorage'] !== null;**
    } catch (e) {
     return false;
    }
    }

**HTML5 STORAGE SUPPORT**

|IE|	FIREFOX	|SAFARI|	CHROME|	OPERA|	IPHONE	|ANDROID|
|---|--------|-------|---------|-----|---------|--------|
|8.0+|	3.5+|	4.0+|	4.0+|	10.5+|	2.0+|	2.0+|

## TRACKING CHANGES TO THE HTML5 STORAGE AREA

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

The storage event is supported everywhere the localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener (although that will finally be added in IE 9). Therefore, to hook the storage event, you’ll need to check which event mechanism the browser supports. (If you’ve done this before with other events, you can skip to the end of this section. Trapping the storage event works the same as every other event you’ve ever trapped. If you prefer to use jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)

    if (window.addEventListener) {
     window.addEventListener("storage", handle_storage, false);
    } else {
     window.attachEvent("onstorage", handle_storage);
     The handle_storage callback function will be called with a StorageEvent object, except in Internet Explorer where the event object is stored in window.event.
    function handle_storage(e) {
    if (!e) { e = window.event; }
    }

At this point, the variable e will be a StorageEvent object, which has the following useful properties.

## LIMITATIONS IN CURRENT BROWSERS

In talking about the history of local storage hacks using third-party plugins, I made a point of mentioning the limitations of each technique, such as storage limits. I just realized that I haven’t mentioned anything about the limitations of the now-standardized  HTML5 Storage. I’ll give you the answers first, then explain them. The answers, in order of importance, are “5 megabytes,” “QUOTA_EXCEEDED_ERR,” and “no.”

## HTML5 STORAGE IN ACTION
Let’s see  HTML5 Storage in action. Recall the Halma game we constructed in the canvas chapter. There’s a small problem with the game: if you close the browser window mid-game, you’ll lose your progress. But with  HTML5 Storage, we can save the progress locally, within the browser itself. Here is a live demonstration. Make a few moves, then close the browser tab, then re-open it. If your browser supports  HTML5 Storage, the demonstration page should magically remember your exact position within the game, including the number of moves you’ve made, the position of each of the pieces on the board, and even whether a particular piece is selected.

How does it work? Every time a change occurs within the game, we call this function:

     function saveGameState() {

    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
    }

The most important part of this function is the caveat that I mentioned earlier in this chapter, which I’ll repeat here: Data is stored as strings. If you are storing something other than a string, you’ll need to coerce it yourself when you retrieve it. For example, the flag for whether there is a game in progress (gGameInProgress) is a Boolean. In the saveGameState() function, we just stored it and didn’t worry about the datatype:

    localStorage["halma.game.in.progress"] = gGameInProgress;

But in the resumeGame() function, we need to treat the value we got from the local storage area as a string and manually construct the proper Boolean value ourselves:

    gGameInProgress = (localStorage["halma.game.in.progress"] == "true");

Similarly, the number of moves is stored in gMoveCount as an integer. In the saveGameState() function, we just stored it:

    localStorage["halma.movecount"] = gMoveCount;

But in the resumeGame() function, we need to coerce the value to an integer, using the parseInt() function built into JavaScript:

    gMoveCount = parseInt(localStorage["halma.movecount"]);
    
## FURTHER READING
### HTML5 storage:

* HTML5 Storage specification
* Introduction to DOM Storage on 
* 
**MSDN**

* Web Storage: easier, more powerful client-side data storage on Opera Developer Community

* DOM Storage on Mozilla Developer Center. (Note: most of this page is devoted to Firefox’s prototype implementation of a globalStorage object, a non-standard precursor to localStorage. Mozilla added support for the standardlocalStorage interface in Firefox 3.5.)

* Unlock local storage for mobile Web applications with HTML5, a tutorial on IBM DeveloperWorks

Early work by Brad Neuberg et. al. (pre- HTML5):

* Internet Explorer Has Native Support for Persistence?!?! (about the userData object in IE)
* Dojo Storage, part of a larger tutorial about the (now-defunct) Dojo Offline library
* dojox.storage.manager API reference
* dojox.storage Subversion repository


**Web SQL Database:**

* Web SQL Database specification
* Introducing Web SQL Databases
* Web Database demonstration
* persistence.js, an “asynchronous JavaScript 
ORM” built on top of Web  SQL Database and Gears

**IndexedDB:**

* Indexed Database API specification
* Beyond HTML5: Database APIs and the Road to IndexedDB
* Firefox 4: An early walk-through of IndexedDB
* This has been “The Past, Present & Future of Local Storage for Web Applications.” The full table of contents has more if you’d like to keep reading.

**DID YOU KNOW?**

In association with Google Press, O’Reilly is distributing this book in a variety of formats, including paper, ePub, Mobi, and  DRM-free  PDF. The paid edition is called “HTML5: Up & Running,” and it is available now. This chapter is included in the paid edition.

If you liked this chapter and want to show your appreciation, you can buy “HTML5: Up & Running” with this affiliate link or buy an electronic edition directly from O’Reilly. You’ll get a book, and I’ll get a buck. I do not currently accept direct donations.    
    
































