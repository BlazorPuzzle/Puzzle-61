# Blazor Puzzle #61

## Wrangling Resources

YouTube Video: https://youtu.be/https://youtu.be/KgSneDfyFD0

Blazor Puzzle Home Page: https://blazorpuzzle.com

### The Challenge:

We are attempting to provide translations for this application. Unfortunately it looks like we're running into a number of errors while we're trying to get it to compile and resolve the translations that we've provided.

Can you fix the error that's happening on the home page and get the translations to display correctly?

### The Solution:

The problem is in *Program.cs*:

```c#
// The solution is to not to specify the resources path. 
// It confuses the localization system.

//builder.Services.AddLocalization(options => options.ResourcesPath = "Resources");
builder.Services.AddLocalization();
```

Boom!
