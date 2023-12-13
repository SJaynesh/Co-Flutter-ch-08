# CH - 8	E-Commerce App

<br><br>

> * Dummy Json website to collect dummy product data.

<br>

## Align Widget :

<br>

> * The Align widget in Flutter aligns a child widget within a parent widget.
> * The alignment can be specified using the alignment property, which takes an Alignment object


<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-08/assets/115562979/916ddf69-d7d9-45b8-87b3-5131985c24f4.png" width=60% height=100%></p>

<br>

<pre>
  body: Align(
            alignment: Alignment.bottomRight,
            child: Text("Hello Flutter"),
        ),
</pre>

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-08/assets/115562979/76681176-d243-4fd4-963c-97851672e6cc.png" width=80% height=60%></p>

<br>

<pre>
  // Center
   body: const Align(
            alignment: Alignment(0, 0),
            child: Text("Hello Flutter"),
          ),

  // Center Left
   body: const Align(
            alignment: Alignment(-1, 0),
            child: Text("Hello Flutter"),
          ),

  // Center Right
  body: const Align(
            alignment: Alignment(1, 0),
            child: Text("Hello Flutter"),
          ),

  // Top Center
   body: const Align(
            alignment: Alignment(0, -1),
            child: Text("Hello Flutter"),
          ),

  // Top Left
   body: const Align(
            alignment: Alignment(-1, -1),
            child: Text("Hello Flutter"),
          ),

  // Top Right
  body: const Align(
            alignment: Alignment(1, -1),
            child: Text("Hello Flutter"),
          ),
  
</pre>











