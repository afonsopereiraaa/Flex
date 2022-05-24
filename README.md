
<h1 align="center">
  <br>
  <br>
  Flex
  <br>
</h1>

<h4 align="center">A Flexible programming language</h4>

<p align="center">
  </a>
  <img src="https://github.com/flexplang/Flex/raw/main/static.png"></a>
  <a href="https://gitter.im/flexprg/community?utm_source=share-link&utm_medium=link&utm_campaign=share-link"><img src="https://badges.gitter.im/amitmerchant1990/electron-markdownify.svg"></a>
  </a>
</p>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#download">Download</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a>
</p>

## Key Features

* Easy to learn and use
* Easy to install
* Flexible
* Cross-Compatible "In the next days"
## How To Use

Downloading or installing is very simple, here is how depending on your version and operating system:

Windows

Navigate to the most recent release and download Flex-Win-Installer.zip.
Unzip Flex-Win-Installer.zip and open the unzipped folder.
Inside is a single file titled Flex-Setup.exe. Run it, and follow the setup instructions.
Now that it is installed, there are a few ways to use it:
(recommended) Any Flex file that ends with .ZS will automatically be associated with the interpreter. Just double-click it, and the interpreter will run.
Drag and drop any .ZS script directly onto the executable in your desktop.
Use command line, providing path to interpreter and then to script like so: > ./Flex.exe example.ZS

Linux

Coming in the next days ;)

> **Note**
> If you can´t run the installer you can just download from the github.


## Download

You can [download](https://github.com/flexplang/Flex/releases/tag/Latest) the latest installable of Flex here

## Here is some example code:
```c++
// Comments are indicated by two forward slashes
// They can only be on their own line
//    int j = 4 // <- This is invalid comment placement

// All programs start with a main function
func Main()
{
    int i = 0
    string s = "r"
    
    i += 2
    i -= 1
    i /= 3
    i *= 2
    
    while i < 10
    {
        i += 1
    }
    
    if s == "r"
    {
        print s + " is r"
    }
    
    int functionNumber = ExampleFunction("A", s)
    ExampleFunction(1, 3)
    
    GlobalFunction()
}

// Declare new function with 'func', then it's name, and the names of any input variables.
// The input variables don't need type, as those are automatic. Also, they don't need to
/// be assigned at all on execute and can be left blank
func ExampleFunction(inputA, inputB)
{
    print "In A is: " + inputA
    print "In B is: " + inputB
    
    // Return a value to the valling location
    return 4
}

func GlobalFunction()
{
    // Create variables that can be accessed from anywhere (ex. in Main or ExampleFunction) with the 'global' keyword before type
    global int x = 12
    global string y = "Y String"
}
```
Here is how to use graphics:
```c++
func Main()
{
    int screenWidth = 500
    int screenHeight = 500
    ZS.Graphics.Init("Title of window", screenWidth, screenHeight)
    // After graphics are initialized, the main function will not finish.
    // Instead, Start() will be called a single time, then Update() every frame after that.
}

// Runs once at start of graphics initialization
func Start()
{
    // Vec2 are initialized using function 'NVec2(x, y)'
    Vec2 position = NVec2(250, 250)
    Vec2 scale = NVec2(20, 20)
    float rotation = 0

    // Sprite object, stores (and loads from file) the texture, location, scale, and rotation
    global Sprite exampleSprite = ZS.Graphics.Sprite("./square.png", position, scale, rotation)
}

// Executes each frame
func Update(deltaTime)
{
    // Draws the image created in Start(). This is usually at the end of update.
    ZS.Graphics.Draw(exampleSprite)   
}
```
Currently, Flex is ***VERY*** strict with formatting, and can throw an error if you forget to put a space somewhere.
Also, speaking of errors, if your code has any it will show in the console. Errors are colored red, and warnings are colored yellow. A line number will also usually be provided. This is ***Not*** the line relative to the *documents* beginning, but rather the *functions* beginning.
Example:
```
ERROR: line 5 in function Main
```
This is the 5th line *inside of Main*.
```c++
func Main()
{
   // line 1
   // line 2
   // line 3
   // line 4
   int g = "s"
   // ^ above line is the error, since it is line 5
}
```
I am planning to change how error reporting works to report the document line number as well, but this is how it is for now.

I left a pong example game in the repository so you can check out :)


## Credits

This software uses the following open source packages:

- [C++](https://cplusplus.com/)
- [SDL2](https://nodejs.org/)
- [SDL2_TTF](https://github.com/chjj/marked)
- [SDL2_image](http://showdownjs.github.io/showdown/)

## License

MIT

---

> GitHub [@flexplang](https://github.com/amitmerchant1990) &nbsp;&middot;&nbsp;
> Twitter [@flexplang](https://twitter.com/flex_plang)

