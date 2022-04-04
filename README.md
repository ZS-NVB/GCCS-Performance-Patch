# CS-Performance-Patch
A performance patch for GemCraft Chasing Shadows which makes the game run something like 10x faster

Besides making the game run much faster, intended mechanical changes are minimal:
* Towers fire at the weakest beacon first because the bug which made that not the case caused lag
* Towers can't fire at guardians if there's monsters in range and they're not set to target specials

In order to make the game run better, some rendering changes were needed:
* Swarmlings which aren't rendered won't have their shield rendered either
* Render limit per tile is set to 1 on min settings rather than 2, like what the sliders allow
* Draw shields option ignores force min/max settings so you can disable it when on force min settings
* An option to enable/disable drawing monster upper body parts is added
* Disabling rendering monster parts will make them not update so they'll be wrong for a few frames when turning them on after they've been disabled

## Installation:

Put all the files into the same folder as the game's swf (gc-cs-steam.swf) and run applypatch

In order for it to work, you will need at least one of the following:
* gc-cs-steam.swf to be the same as the game's original swf
* gc-cs-steam-unmodified.swf to exist and be the same as the game's original swf
* gc-cs-steam-uncompressed.swf to exist and be the game's original swf after being decompressed

After applying the patch successfully:
* gc-cs-steam.swf will be patched
* gc-cs-steam-unmodified.swf will be a copy of the game's original swf
* gc-cs-steam-uncompressed.swf will be a decompressed version of the game's original swf

gc-cs-steam-unmodified.swf won't be created if gc-cs-steam-uncompressed.swf already existed because only gc-cs-steam-uncompressed.swf is actually needed for the patch

gc-cs-steam-unmodified.swf can be deleted if you don't care about having a copy of the original swf since gc-cs-steam-uncompressed.swf is just that but decompressed so it will function the same

## Disclaimer:

Uses Courgette: https://chromium.googlesource.com/chromium/src/courgette/

and RABCDAsm: https://github.com/CyberShadow/RABCDAsm

```
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
