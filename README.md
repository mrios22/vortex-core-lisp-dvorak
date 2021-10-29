# A Vortex CORE configuration for Dvorak, Emacs, and Lisp Programming

### Marc Rios

![A Vortex CORE configuration for Dvorak, Emacs, and Lisp](https://github.com/mrios22/vortex-core-lisp-dvorak/blob/main/vortex-dvorak-lisp.jpg?raw=true)

## Introduction

 I customized and reprogrammed my Vortex CORE 40 for the following:

 * Typing with the Dvorak keymap.
 * Using GNU Emacs.
 * Writing lisp programs.
 * Entering numbers quickly using a numeric keypad.
 
 This README explains my configuration and how you can copy it onto your board. You can program it onto your board key by key using a MPC tool (recommended, so you learn about the setup) or you can upload my config file.
 
## Initial Configuration of a New CORE
 
Before you start programming the keyboard you must install the new [firmware]{http://www.vortexgear.tw/vortex3.asp). Using a Windows computer, go to the Vortex website, download the firmware ``.exe``, and install the ``CORE MPC`` option.

Then go to [TcFreddie's Much Programming Core webpage](https://tsdo.in/much-programming-core/). We will be using it to configure the board. (If you want to skip the programming and upload my configuration onto your board, skip to the last step.)
 
## Guide to the Layers (and some design principles) 

Layer ``L0`` will be the Dvorak/Emacs layer. 

Layer ``L1`` will be a vanilla layer: the keymappings will match what is printed on the keyboard. (Sometimes you need to hand your keyboard to someone else and you want them to be able to use it. Or sometimes you have to enter a complicated password and you don't want to touch type it.)

Layer ``L2`` will be the same as ``L1`` until I figure out something better to do with it.

Layer ``L3`` will be a mapping with a numeric keypad, an arrow keypad, and a few other convenient things. 
 
 When I was planning the keymapping, I followed three principles:
 
* Keep the Dvorak keymapping as intact as possible for the alphabet and for normal English punctuation. 
* If multiple keys need to be pressed, try to limit it to two keys. Avoid using the same hand to press multiple keys simultaneously. 
* Use ``Fn``, ``Fn1``, and ``Pn`` to access frequently-used characters. Place these frequently-used characters on the home row if possible.
 
## Dvorak on the CORE

This keyboard configuration assumes that you can touch type in Dvorak. Almost all of the keycaps will remain in their original position. 

Touch typing on the CORE is easier than it looks. The Vortex CORE does not have homing tabs on the ``F`` and ``J`` keys, but those keys are noticeably more concave than their neighbors. Your brain will eventually be able to notice the slight difference in concavity. After a few days, your index fingers will naturally return to the right place even if you can't see the keyboard.

To use Dvorak on the CORE, you have to reprogram the keyboard and move some keycaps around. Most people who use Dvorak probably use software (namely the OS) to implement the keymapping rather than using a Dvorak keyboard. That won't work with the Vortex CORE. If you do that, you won't have a ``z`` key.

Reprogram  ``L0``. With the Dvorak keys. For most keys this works out fine, but ``z``, ``-_``, and ``/?`` are a problem. Since Dvorak touch typists will expect ``z`` to be where ``Right Shift`` is located, I reprogrammed ``Right Shift`` to be ``z``. (I tried to avoid doing this, but it's the only sane way. Your WPM will drop like a rock if you have to press a modifier key to type lower-case ``z``.) 

Now that ``Right Shift`` is reprogrammed to ``z``, we have to create a ``Right Shift`` key. Dvorak touch typists will expect ``Right Shift`` to be in the default position for ``Fn1``. It is best to move ``Fn1`` elsewhere. I used the keypuller to swap ``Right Alt`` with ``Fn1``. I programmed all four of the keyboard's layers so the ``Fn1`` location is correct. Then in ``L0`` I reprogrammed the key with the ``Right Alt`` cap so it is the ``Right Shift``. In all other layers I reprogrammed it to be ``Right Alt``.

We will also want easy access to ``/?``. I reprogrammed ``Delete`` so it  maps to ``/?``. Dvorak touch typists will expect the key to be there. ``?`` is used so frequently that we shouldn't have to press three keys to access it. I never use the ``Delete`` key, so this wasn't a significant loss for me. (To keep ``Delete`` available for those who might miss it, I programmed in the keymapping ``Pn + Delete`` = ``Delete`` .)

The final adjustment we need to make is to get easier access to the ``-_`` key. The ``-`` character is used so frequently in programming that it will be annoying to have to press ``Fn1 + ;`` to get it. That's a bad combo for a character that is used so frequently. To do that combination you need to either remove your fingers from the home row or press a key combination using the thumb and pinky of the right hand simultaneously (this will definitely cause cramps). To avoid the handstrain, I reprogrammed ``L0`` so pressing ``Pn + ;``will yield ``-``. With some practice, it becomes very easy to reach the thumb over to the ``Pn`` key when you need to type ``-``.

``Fn1`` is not in a great location. It would have been better to place it to the right of the ``Space`` bar, but the position of ``Fn`` cannot be changed. I recommend that you train yourself not to use your thumb to press this ``Fn1``. Use your right ring finger instead. Your right thumb will get tired of reaching for this key.

After adopting this setup, I was able to get back up to my normal WPM within two days. The hardest part was getting used to the location of ``-``. It was also difficult to get used to using ``Fn1``. (Hint: writing a long article in Markdown is a good way to practice touch-typing special characters using ``Fn1``.)

## Emacs CORE

It is easy to reconfigure the CORE for Emacs. First, reprogram the ``Left Space`` bar as a ``Ctrl`` in layer ``L0``. It will take some time to get used to having the ``Ctrl`` in that location, but after you get used to it, it will save you a lot of fingerstrain.

The next thing I did was to physically swap the locations of ``Esc`` and ``Left Alt`` (Meta). After one day of using Emacs on the CORE, I knew that the ``Left Alt`` key had to be moved. My left thumb was suffering from pressing the ``Left Alt`` key in that location. Placing the meta key in the upper left-hand corner was a far better choice. I reprogrammed layers ``L0-L2`` to match the physical key configuration of ``Esc`` and ``Left Alt``. The downside of making the keycap switch is that the `` `~`` key text is in the wrong location. It looks incongruous with the rest of the board. 
I reprogrammed the key so its function matches what is printed on it, but I kept the  `` `~`` key stored in the ``Fn1`` layer of the ``Left Alt`` keycap in the upper left corner of the keyboard.

## Lisp and Clojure Programming

To program in Lisp and Clojure, you must have easy access to the symbols ``()[]{}-_"=+#%``. I reprogrammed the home row and ``zxcv`` keys of ``L0`` to give me easy access to these symbols. ``Left Shift`` has also been modified. To get access to these symbols, you need to press ``Fn`` or ``Pn``, depending on the side of the board that you are using. (The mappings are designed so you will use one finger from each hand to do the key combination rather than two fingers from the same hand.) This may make it easier to reach common programming symbols on the Vortex CORE than it is to reach them on your normal keyboard.

(The left hand side of the equation shows which QWERTY keycaps to press.)

 * ``Fn + a`` = ``{``
 * ``Fn + s`` = ``}``
 * ``Fn + d`` = ``[``
 * ``Fn + f`` = ``]``
 * ``Pn + j`` = ``*``
 * ``Pn + k`` = ``(``
 * ``Pn + l`` = ``)``
 * ``Pn + ;`` = ``-``
 * ``Pn + Enter`` = ``+``
 * ``Fn + z`` = ``(``
 * ``Fn1 + z`` = ``)``
 * ``Fn + x`` = ``[``
 * ``Fn1 + x`` = ``]``
 * ``Fn + c`` = ``{``
 * ``Fn1 + c`` = ``}``
 * ``Fn + v`` = ``#``
 * ``Fn1 + v`` = ``%``
 * ``Fn + Tab`` = ``_``
 * ``Fn + Left Shift`` = ``"``
 
 To program these properly, you must use macros. The MPC tool makes it easy to create macros. Be sure to rearrange the order of the up and down strokes so two keys are held simultaneously rather pressed one after the other.
 
 If you use Emacs to write lisp programs, you probably use smartparens mode or paredit mode. (If you don't, you should!) One of the best features of these modes is that you can move paretheses around to change scope. The Emacs command for moving paretheses around are ``Ctrl + (`` and ``Ctrl + )``. Entering these keyclicks is a nightmare even on my modified board. I created two macros for these commands.
 
* ``Pn + Right Win`` = ``Ctrl + <-``
* ``Pn + Right Ctrl`` = ``Ctrl + ->``

I chose to put these keys in the lower right corner because that is usually where the arrow keys are a keyboard. Lisp programmers will have a lot of muscle memory trained to find the arrow keys there.
 
## L3: The numeric keypad and arrow pad layer.

![A Vortex CORE configuration for Dvorak, Emacs, and Lisp (L3)](https://github.com/mrios22/vortex-core-lisp-dvorak/blob/main/l3-number-pad.jpg?raw=true)

Occasionally I need to enter data using a numeric keypad. I reprogrammed ``L3`` with a keypad on the left-hand-side. 

I also added an arrow keypad. When in ``L3``, the arrow keys on keycaps ``ijkl`` work as if it is a normal arrow keypad. 

To get easy access to the arrows and numeric keypad, I programmed the ``Right Win`` button to serve as a toggle between ``L3`` and ``L0``. If you are entering a number more than a few digits long, then it makes sense to toggle layers. If you will be using the arrow keys for a while, definitely toggle the layers. 

## Installing this keyboard configuration.

If you would like to copy my configuration rather than programming it in yourself, you can download ``vortex-core-dvorak.json`` from this repository and then upload it into TcFreddie's MPC webpage. Download the binary code from the webpage. Unplug your keyboard, hold down the ``Fn + d`` keycaps, and plug the board back in. Your OS should recognize the keyboard as a storage device. Delete the file on that storage device and replace it with the binary file you downloaded from the MPC page. Eject the drive. Disconnect and then reconnect the keyboard. Your keyboard should now be programmed with my configuration. 
