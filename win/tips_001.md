1. Assign integer to a boolean type variable will cause unnecessary performance issue. If needed, using integer instead of boolean.
2. XINPUT will stall if specific index of controller is not connected. Thus, only check the states of connected controllers
3. **VBlank**: In a raster graphics display, the vertical blanking interval (VBI), also known as the vertical interval or VBLANK,  
is the time between the end of the final line of a frame or field and the beginning of the first line of the next frame.   
It is present in analog television, VGA, DVI and other signals. During the VBI, the incoming data stream is not displayed on the screen.  
In raster cathode ray tube displays, the beam is blanked to avoid displaying the retrace line; see raster scan for details.  
The signal source, such as a television broadcast, does not supply image information during the blanking period.

4. **COM** : [Component Object Model](https://msdn.microsoft.com/en-us/library/windows/desktop/ms694363.aspx).
COM is MicroSoft's c++ implementation across the dll boundary

## [How to declare vtbl in c](https://hero.handmade.network/forums/code-discussion/t/920-directsound_and_c)

## [Paste two worlds together in macro](https://www.cprogramming.com/reference/preprocessor/token-pasting-operator.html)

--------

Go and download Intel Developer Manual for reference.

## Ways to measure performance

[Clock Counter: RDSTC](https://c9x.me/x86/html/file_module_x86_id_278.html)

[QueryPerformanceCounter](https://msdn.microsoft.com/en-us/library/windows/desktop/ms644904.aspx)

## Print out variables in windows
```
char Buffer[256];
wsprintf(Buffer, "%d", x);
OutputDebugStringA(Buffer);
```

_NOTE:_ [ETW](https://docs.microsoft.com/en-us/dotnet/framework/wcf/samples/etw-tracing)

[A Good Blog](https://tomforsyth1000.github.io/blog.wiki.html)

* You can inject pound define in compile command
* Do not heavily rely on macro to realize cross-platform code. It dictats control flow must be equivalent across all platform.
* Unity Build: The entire project only has one conceptual translation unit.
	* Speed up compiling, and good for optimizer.
* 11ms per frame -> VR; 16ms per frame -> 60fps smoothy; 33ms per frame -> 30 fps;
* Flexibility determines the time to inverse the way we thinking
* OCD?