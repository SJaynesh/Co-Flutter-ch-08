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

  
  // Bottom Center
  body: const Align(
          alignment: Alignment(0, 1),
          child: Text("Hello Flutter"),
        ),

  // Bottom Left
   body: const Align(
          alignment: Alignment(-1, 1),
          child: Text("Hello Flutter"),
        ),


  // Bottom Rigth
   body: const Align(
          alignment: Alignment(1, 1),
          child: Text("Hello Flutter"),
        ),
</pre>

<br><br>

## Container Widget: 

<br>

<pre>
  body: Align(
          child: Container(
            height: 180,
            width: 180,
            color: Colors.blue.shade400,
          ),
        ),
</pre>

<br><br>

### Nasted Container:

<br>

<pre>
  body: Align(
          child: Container(
            height: 180,
            width: 180,
            color: Colors.blue.shade400,
            alignment: Alignment.center,
            child: Container(
              height: 150,
              width: 150,
              color: Colors.blue.shade200,
              alignment: Alignment.center,
              child: Container(
                height: 100,
                width: 100,
                color: Colors.white,
                alignment: Alignment.center,
                child: Text("Hello Flutter"),
              ),
            ),
          ),
        ),
</pre>

<br>

## BoxDecoration class:

<br>

### `Border:`

<br>

 #### Border.all

 <br>

 <pre>
   body: Align(
          child: Container(
            height: 180,
            width: 180,
            decoration: BoxDecoration(
              color: Colors.blue.shade400,
              border: Border.all(
                color: Colors.purpleAccent,
                width: 5,
              ),
            ),
            alignment: Alignment.center,
            child: const Text("Hello Flutter"),
          ),
        ),
 </pre>

 <br>

 #### Border

<br>

<pre>
  body: Align(
          child: Container(
            height: 180,
            width: 180,
            decoration: BoxDecoration(
              color: Colors.blue.shade400,
              border: Border(
                top: BorderSide(
                  color: Colors.yellowAccent,
                  width: 10,
                ),
                bottom: BorderSide(
                  color: Colors.red,
                  width: 10,
                ),
                left: BorderSide(
                  color: Colors.orangeAccent,
                  width: 10,
                ),
                right: BorderSide(
                  color: Colors.cyanAccent,
                  width: 10,
                ),
              ),
            ),
            alignment: Alignment.center,
            child: const Text("Hello Flutter"),
          ),
        ),
</pre>

<br>

#### Border.symmetric

<br>

<pre>
  body: Align(
          child: Container(
            height: 180,
            width: 180,
            decoration: BoxDecoration(
              color: Colors.blue.shade400,
              border: Border.symmetric(
                vertical: BorderSide(
                  color: Colors.indigo,
                  width: 30,
                ),
                horizontal: BorderSide(
                  color: Colors.redAccent,
                  width: 30,
                ),
              ),
            ),
            alignment: Alignment.center,
            child: const Text("Hello Flutter"),
          ),
        ),
</pre>

<br>

<pre>
  body: Align(
          child: Container(
            height: 180,
            width: 180,
            decoration: BoxDecoration(
              color: Colors.blue.shade400,
              border: Border.symmetric(
                vertical: BorderSide(
                  color: Colors.yellow,
                  width: 105,
                ),
                horizontal: BorderSide(
                  color: Colors.pink,
                  width: 105,
                ),
              ),
            ),
            alignment: Alignment.center,
            child: const Text("Hello Flutter"),
          ),
        ),
</pre>

<br><br>

## Types of Widgets (StatelessWidget & StatefulWidget):

<br>

### `StatelessWidget :`

<br>

> * `Perform changes on screen only while hotreload.`
> * This is a kind of widget which is static and only created once in a memory
> * Using this widget we cannot update an UI.
> * Since this widget did not created in memory frequently, this supplies rapid performance as compared to StatefulWidget.
> * This widget contains only one lifecycle method, build() method.

<br><br>

### Syntax:

<pre>
  class [MyApp] extends StatelessWideget 
  {
    const [MyApp]({Key?key}):super(key:key);

    @override
    Widget build(BuildContext context) {
      return UIPage();
    }
  }
</pre>

<br>

> 1. `extends: ` inherite StatelessWidget
> 2. `super: ` Parent class Constructor


### Reload:
> * Only for build method is called in reload.

<br>

### Refresh(RUN):
> * Run the entire code from the references.


<br><br>

## `StatefullWidget:`

<br>

> * `Performs changes on screen every time using setState((){}); function.`
> * This is a kind of widget which is dynamic and placed inside a memory (RAM).
> * Using this widget we can update an UI using its lifecycle method setState().
> * Since this widget did created in memory frequently, this supplies slow performance as compared to StatelesWidget.

<br>

> * This widget contains 5 lifecycle methods, such as
> * `createState();`
> * `initState();`
> * `build();`
> * `setState();`
> * `dispose();`


<br>

### Syntax:

<pre>
  class [MyApp] extends StatefullWidget
  {
      const [MyApp]({Key?key}) : supeer(key?key);

      State<[MyApp]> createState() => _[MyApp]State();
  
  }

  class _[MyApp]State extends State<[MyApp]>
  {

    @override
    initState() {
      super.initState();
    }

    @override
    Widget build(BuildContext context)
    {
      return UIPage();
    }
  }
</pre>


<br><br>

## Lifecycle of Statefullwidget

<br>

### 1. createState()

<br>

> * This method is responsible to provide UI page to main function.
> * It executes when we start the application.


<br>

### 2. initState()

<br>

> * This method is executed after createState() and before build method.
> * It will be again called or execute when we redirect to the page again.
> * This method is mainly responsible to reassigned over variables.

<br>

### 3. Build()

<br>

> * This method is called after initState.
> * This method contains over UI page which we want to change frequently.
> * can be re-invoked by reloading the UI using hot-reload or setState()
> * contains BuildContext of the UI


<br>

### 4. setState()

<br>

> * All the changes of UI can be applied using setState();
> * can be used number of times to reload the ui.
> * every expression which is updating the data must be written in setState()


<br>

### 5. dispose()

<br>

> * This method is responsible to clear memory space of variables or objects from RAM.
> * similar as destructor, it is responsible to dispose(free-up/destroy) all the variable or controllers which means to be erased while leaving the page or app.
> * This method is called at the end of current page.



<br><br><br><br><br>

## `Routing :`

<br>

> * In any mobile app, navigating to different pages defines the workflow of the application, and the way to handle the navigation is known as routing.
> * Routes are used to navigate from one page to another.
> * Flutter provides a basic routing class MaterialPageRoute and two methods Navigator. push() and Navigator. pop()


<br><br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-08/assets/115562979/4a4822c6-e255-46b3-bc6a-5f5eda0b5285.png" width=80% height=100%></p>

<br><br>

## `Types of Routing :`

<br>

> 1. Default Routing
> 2. Named Routing
> 3. onGenerateRouting

<br><br>

## 1. Default Routing :

<br>

> * Use the Navigator class to navigate from one page to another.

<br>

### Navigator class provide the Three methods:

<br>

> 1. Push
> 2. Pop
> 3. PushAndRemoveUntil

<br>

#### Push : 

<br>

> * To switch to a new route, use the Navigator.push() method.

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-08/assets/115562979/5bcccaea-4e05-4a90-98de-925a182739d1.png" width=100% height=80%></p>

<br>

#### Pop :

<br>

> * Navigator.pop() method. The pop() method removes the current Route from the stack of routes managed by the Navigator.

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-08/assets/115562979/34d9a3c0-640a-429a-a8b8-6b3e45466e47.png" width=100% height=80%></p>

<br>

#### PushAndRemoveUntil :

<br>

> * Navigator.pushAndRemoveUntil removes all the routes despite conditions.

<br>

<p><img src = "https://github.com/SJaynesh/Co-Flutter-ch-08/assets/115562979/d3e980d3-91a0-4d8e-b90f-37aa72433e96.png" width=100% height=80%></p>

<br>








