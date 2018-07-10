# KeystrokeAPI
A simple Keystroke API written in C# that works for any version of Windows. It abstracts the access to the *win32.dll* and the handling of low level hooks (only keyboard for now). ``

## Code Example (using a Console Application) 
```c#
class Program
{
    static void Main(string[] args)
    {
        using (var api = new KeystrokeAPI())
        {
            api.CreateKeyboardHook((character) => { Console.Write(character); });
            Application.Run();
        }
    }
}
```
