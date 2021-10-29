# A Vortex CORE configuration for Dvorak, Emacs, and Lisp Programming

### Marc Rios (marcrios@fastmail.com)

## Introduction

 I customized and reprogrammed my Vortex CORE 40 for the following:

 * Typing with the Dvorak keymap.
 * Using GNU Emacs.
 * Writing lisp programs.
 * Entering numbers quickly using a numeric keypad.
 
 This README explains my configuration and how you can copy it on your board.
 
## Initial Configuration of a New CORE
 
Before you start programming the keyboard you must install the new firmware. Using a Windows computer, go to the Vortex website, download the firmware ``.exe``, and install the ``CORE MPC`` option.

Then go to TcFreddie's Much Programming Core webpage. We will be using it to configure the board.
 
## Dvorak on the CORE

This keyboard configuration assumes that you can touch type in Dvorak. Almost all of the keycaps will remain in their original position.

Most people who use Dvorak probably use software (namely the OS) to implement the keymapping rather than using a Dvorak keyboard. That won't work with the Vortex CORE. To get a comfortable Dvorak configuration, you have to reprogram the keys and move some keycaps around on the keyboard.

First I program the Dvorak keymap into level ``L0``. For most keys this works out fine, but ``z``, ``-_``, and ``/?`` are a problem. Since Dvorak touch typists will expect ``z`` to be where ``Right Shift`` is located, I reprogrammed ``Right Shift`` to be ``z``. (I tried to avoid doing this, but it's the only sane way. Your WPM will drop like a rock if you have to press a modifier key to type lower-case ``z``.) 

We will also want easy access to ``/?``. I reprogrammed ``Del`` so it  maps to ``/?``. Dvorak touch typists will expect the key to be there. ``?`` is used so frequently that we shouldn't have to press three keys to access it. I never use the ``Del`` key, so this wasn't a significant loss for me.

Now that ``Right Shift`` is reprogrammed to ``z``, we have to create a ``Right Shift`` key. Dvorak touch typists will expect ``Right Shift`` to be in the default position for ``Fn1``. It is best to move ``Fn1`` elsewhere. I used the keypuller to swap ``Right Alt`` with ``Fn1``. I programmed all four of the keyboard's layers so the ``Fn1`` location is correct. Then in ``L0`` I reprogrammed the key with the ``Right Alt`` cap so it is the ``Right Shift``. In all other layers I reprogrammed it to be ``Right Alt``.

The final adjustment we need to make is to get easy access to the ``-_`` key. The ``-`` character is used so frequently in programming that it will be annoying to have to press ``Fn1 + ;`` to get it. I reprogrammed ``L0`` so pressing ``Pn + ;``will yield ``-``. With some practice, it becomes very easy to reach the thumb over to the ``Pn`` key when you need to type ``-``.

One inconvenient aspect of this setup is that ``Fn1`` is not in a great location. It would have been better to place it to the right of the ``Space`` bar, but the position of ``Fn`` cannot be changed. I recommend that you train yourself not to use your thumb to press this ``Fn1``. Use your right ring finger instead. Your right thumb will get tired of reaching for this key.

After adopting this setup, I was able to get back up to my normal WPM within two days. The hardest part was getting used to the location of ``-``. 

## Emacs CORE

It is easy to reconfigure the CORE for Emacs. First, reprogram the ``Left Space`` bar as a ``Ctrl`` in layer ``L0``. It will take some time to get used to having the ``Ctrl`` in that location, but after you get used to it, it will save you a lot of fingerstrain.

The next thing I did was to physically swap the locations of ``Esc`` and ``Left Alt`` (Meta). After one day of using Emacs on the CORE, I knew that the ``Left Alt`` key had to be moved. My left thumb was suffering from pressing the ``Left Alt`` key in that location. Placing the meta key in the upper left-hand corner was a far better choice. I reprogrammed layers ``L0-L2`` to match the physical key configuration of ``Esc`` and ``Left Alt``. The downside of making the keycap switch is that the `` `~`` key text is in the wrong location. 
I reprogrammed the key so its function matches what is printed on it, but I kept the  `` `~`` key stored in the ``Fn1`` layer.

## Lisp and Clojure Programming

