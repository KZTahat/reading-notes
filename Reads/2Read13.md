# Local Storage
<!-- “The Past, Present, and Future of Local Storage for Web Applications” -->
Persistent local storage is one of the areas where native client applications have held an advantage over web applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files, or some other place according to platform convention. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions.<br />
What we really want is:<br />
- a lot of storage space
- on the client
- that persists beyond a page refresh
- and isn’t transmitted to the server<br />
<br /><br />

- **A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5**:<br />
    In the beginning, there was only Internet Explorer. Or at least, that’s what Microsoft wanted the world to think. To that end, as part of the First Great Browser Wars, Microsoft invented a great many things and included them in their browser-to-end-all-browser-wars, Internet Explorer. One of these things was called DHTML Behaviors, and one of these behaviors was called userData.<br />

    In 2002, Adobe introduced a feature in Flash 6 that gained the unfortunate and misleading name of “Flash cookies.” Within the Flash environment, the feature is properly known as Local Shared Objects. Briefly, it allows Flash objects to store up to 100 KB of data per domain. Brad Neuberg developed an early prototype of a Flash-to-JavaScript bridge called AMASS (AJAX Massive Storage System), but it was limited by some of Flash’s design quirks. By 2006, with the advent of ExternalInterface in Flash 8, accessing LSOs from JavaScript became an order of magnitude easier and faster. Brad rewrote AMASS and integrated it into the popular Dojo Toolkit under the moniker dojox.storage. Flash gives each domain 100 KB of storage “for free.” Beyond that, it prompts the user for each order of magnitude increase in data storage (1 Mb, 10 Mb, and so on).<br />

    As you survey these solutions, a pattern emerges: all of them are either specific to a single browser, or reliant on a third-party plugin. Despite heroic efforts to paper over the differences (in dojox.storage), they all expose radically different interfaces, have different storage limitations, and present different user experiences. So this is the problem that HTML5 set out to solve: to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.<br />

- **INTRODUCING HTML5 STORAGE**:<br />
    What I will refer to as “HTML5 Storage” is a specification named Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons. Certain browser vendors also refer to it as “Local Storage” or “DOM Storage.” The naming situation is made even more complicated by some related, similarly-named, emerging standards that I’ll discuss later in this chapter.<br />

    So what is HTML5 Storage? Simply put, it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.<br />

    From your JavaScript code, we can access HTML5 Storage through the localStorage object on the global window object. Before we can use it, we should detect whether the browser supports it.<br />
    
    ```
        function supports_html5_storage() {
        try {
            return 'localStorage' in window && window['localStorage'] !== null;
        } catch (e) {
            return false;
        }
        }
    ```
    <br />

- **USING HTML5 STORAGE**:<br />
    HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.<br />

    ```
    interface Storage {
        getter any getItem(in DOMString key);
        setter creator void setItem(in DOMString key, in any data);
    };
    ```
    <br />

    Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.<br />

    There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).<br />

    ```
    interface Storage {
        deleter void removeItem(in DOMString key);
        void clear();
    };
    ```
    <br />
    Calling removeItem() with a non-existent key will do nothing.<br />

    Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).<br />

    ```
    interface Storage {
        readonly attribute unsigned long length;
        getter DOMString key(in unsigned long index);
    };
    ```
    <br />
    If you call key() with an index that is not between 0–(length-1), the function will return null.<br />
    <br />

    [Home]( https://kztahat.github.io/reading-notes/)