# Clearing the Screen
To clear the screen use ```
``` C
#include <ti/screen.h>
int main(void) {
	os_ClrHome();
	return 0;
}
```
# Writing to the Screen
To write to the screen, first locate the VRAM at **address:0xD40000** and then you'll have access to a 320x240 display with 2 bit RGB color scheme. 5 bits for blue 6 bits for green and 5 bits for red. Important to note that green only uses 5 of the 6 bits.
``` C
	uint16_t *vram = (uint16_t*)0xD40000;
    /* Clear the homescreen */
    os_ClrHome();
    
    uint16_t color = RGB(255u, 0u, 0u);
	
    for (size_t i = 0; i < WIDTH; i++)
    {
        for (size_t j = 0; j < HEIGHT; j++)
        {
            uint16_t *vram_loc = (vram + (j*WIDTH)+i);
            *vram_loc = color;
        }
    }
```
# Print to Screen
To raw print to screen using OS, use `os_PutStrFull`. 
# Framerate limiting
``` C
    while (!os_GetCSC()) {
        clock_t start = clock();

        printf("GRAPHICS STUFF");
        
        clock_t dt = clock()- start;
        do
        {
            dt = clock()-start;
        } while (dt < FPS(30));
    }
```
