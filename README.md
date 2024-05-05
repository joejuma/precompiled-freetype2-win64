# Freetype 2 Library

## About
This is a built verison of Freetype2, that only has what's necessary to include in a C++ program.

## Usage
1. Add `freetype-2.13.2/include/` to your projects additional includes. You MUST do this directory - other paths use `<>` includes relative to it, so you can't get around this.
2. Add `#include <ft2build.h>` and right after `#include FT_FREETYPE_H` to your includes somewhere in your project.
3. You're all set.

## How It Was Built
This is a note for how it's built using Visual Studio on Windows, since it wasn't 100% straight-forward, should you ever want to build a new version.
1. Download the Freetype repository.
2. Unpack.
3. Go into `freetype-version/builds/windows/vc2010` and open the solution file in Visual Studio.
4. Set your configure to what you want. `Release-Static` was for a static lib file, and make sure you use the right architecture (x64 in this case).
5. It should build just fine.
6. Go to `freetype-version/objs` and you'll see the build folder, or just the prebuilt `freetype.lib` file. Grab whichever `*.lib` you want from this - of course meaning the prebuilt or your newly built one for the right arch and env.
7. Go include that as your static library (what's in the `lib` folder in this package).
8. Make sure you also add the includes to your new repo.
9. All set. That's how this was made.

## Copyright
The code is all freetype, so see their README, README.git and LICENSE file. But the instructions are Copyright Joseph M. Juma 2024, all rights reserved. Also - completely free to use, just don't misrepresent our relationship please.
