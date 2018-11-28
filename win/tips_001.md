1. Assign integer to a boolean type variable will cause unnecessary performance issue. If needed, using integer instead of boolean.
2. XINPUT will stall if specific index of controller is not connected. Thus, only check the states of connected controllers
3. **VBlank**: In a raster graphics display, the vertical blanking interval (VBI), also known as the vertical interval or VBLANK,  
is the time between the end of the final line of a frame or field and the beginning of the first line of the next frame.   
It is present in analog television, VGA, DVI and other signals. During the VBI, the incoming data stream is not displayed on the screen.  
In raster cathode ray tube displays, the beam is blanked to avoid displaying the retrace line; see raster scan for details.  
The signal source, such as a television broadcast, does not supply image information during the blanking period.

4. **COM** : [Component Object Model](https://msdn.microsoft.com/en-us/library/windows/desktop/ms694363.aspx).
COM is MicroSoft's c++ implementation across the dll boundary

5. [How to declare vtbl in c](https://hero.handmade.network/forums/code-discussion/t/920-directsound_and_c)

6. [Paste two worlds together in macro](https://www.cprogramming.com/reference/preprocessor/token-pasting-operator.html)

--------

7. Go and download Intel Developer Manual for reference.

8. Ways to measure performance  
	a. [Clock Counter: RDSTC](https://c9x.me/x86/html/file_module_x86_id_278.html)  
	b. [QueryPerformanceCounter](https://msdn.microsoft.com/en-us/library/windows/desktop/ms644904.aspx)

9. Print out variables in windows  
	```
	char Buffer[256];
	wsprintf(Buffer, "%d", x);
	OutputDebugStringA(Buffer);
	```
	**note**:  
	If extra `%` is put into format string, `wsprintf` will read into stacks it shouldn't read into.  
	`wsprintf` cannot print float numbers (verification needed) 

10. [Event Tracing for Windows](https://docs.microsoft.com/en-us/dotnet/framework/wcf/samples/etw-tracing)

11. [A Good Blog](https://tomforsyth1000.github.io/blog.wiki.html)

12. [LARGE_INTEGER](https://docs.microsoft.com/en-us/windows/desktop/api/winnt/ns-winnt-_large_integer) is an `union`

13. Cast before calculation when:
	```
	int x, y;
	float z = x / y;
	```

14. [MULtiply Packed Single-precision floating-point values](https://www.felixcloutier.com/x86/MULPS.html)  
	When using `floate` instead of `double`, for same amount of work, MULPS faster.

15. [Intrinsic function](https://en.wikipedia.org/wiki/Intrinsic_function)

16. How to make code cross platform  
	1. Different ways:  
		a. Using pre-processor and compile time pund defines

		```
		#if ID_RUNNING_ON_WIN32
			// Stuff in here for win32
		#endif
		```  
		Problem:  
			Not legible.  
			The control flow of your program is shared on all platforms that you will ever ship on.  

		b. Using a virtual abstraction alyer to eliminate the difference between differrent  
		operating systems

		c. Instead of the platform layer being a service to the game, we consider the game as service to the operating system, to produce the graphics and sound to play the game.

17. Unity Build: The entire project only has one conceptual translation unit.
	* Speed up compiling, and good for optimizer.

18. 11ms per frame -> VR; 16ms per frame -> 60fps smoothy; 33ms per frame -> 30 fps;

19. While doing including, put as much as your code before platform specific headers, so that you can make sure your code is well isolated from platform code. aka. You'll know when platform specific code shadows your code.

20. Sound output is like motion blur.

21. User input alawas at least one frame behind.

22. For storing user input sequence, use start/end timestamp and the number of transistions will save us from storing the actual input status info, but on the other hand, we will lose the time info for each input.