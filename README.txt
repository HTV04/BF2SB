BF2SB v2.2.2
By HTV04

BF2SB is a brainf**k converter that converts brainf**k code to SmileBASIC code.

Thanks to phil_ (IAmAPerson620) for the base code. You can download her original program here: 2KE3384V

Also thanks to snail_ (MrCashews) for the REPLACE$() and COUNT() functions from his YARN.LIB library, which can be downloaded here: Q33J44BD

If you want to learn more about brainf**k, look here: https://esolangs.org/wiki/Brainf**k

Instructions:
- Make sure the converter is in SLOT 0.
- Type/load brainf**k code in SLOT 1.
- Run the converter by pressing START.
- Converted code is saved to SLOT 2 and is automatically run.

Options:
- Brainf**k code options:
  - OPTIMIZE:
    - Optimize brainf**k code.
    - Possible values: 0 (off), 1 (on)
    - Default: 1 (on)
  - MEMSIZE:
    - Memory size converted brainf**k code is given.
    - Possible values: any positive integer
    - Default: 30000 (standard)
  - BITWIDTH:
    - Width of bits.
    - Possible values: 0 (8, standard), 1 (16), 2 (32)
    - Default: 0 (8, standard)
  - SIGNEDINT:
    - Choose whether integers are signed or unsigned.
    - Possible values: 0 (unsigned), 1 (signed)
    - Default: 1 (signed)
- Converted code options:
  - SBCOMMENT:
    - Add extra comments to the converted program.
    - Possible values: 0 (off), 1 (on)
    - Default: 1 (on)
  - SBOPTIMIZE:
    - Optimize converted code.
    - Possible values: 0 (off), 1 (on)
    - Default: 1 (on)
  - SBMEMOF
    - Choose how to handle what happens when memory overflows or underflows.
    - Possible values: 0 (wrap), 1 (abort)
    - Default: 0 (wrap)
  - SBCHR13
    - When pointer is at 13, ignore the converted print command (character code 13 is used as a newline on some interpreters, and SmileBASIC only interprets it as a blue curved arrow).
    - Possible values: 0 (off), 1 (on)
    - Default: 1 (on)
  - SBINPUT:
    - Choose how to handle input.
    - Possible values:
      - 0 ("SBINPUT$" is used as input on request, "SBINPUTEOF" applies, standard)
      - 1 (Wait for input)
    - Default: 1 (Wait for input)
  - SBINPUT$:
    - Use as input when "SPINPUT" is set to 0.
    - Possible values: any valid string within quotes
    - Default: ""
  - SBINPUTEOF:
    - Choose how to handle what to set cell to when EOF is reached. Only applies when "SBINPUT" is set to 0.
    - Possible values: 0 (0), 1 (-1), 2 (unchanged, standard)
    - Default: 2 (unchanged, standard)
  - SBWAIT:
    - Enables waiting "WAITCNT" number of frames between instructions.
    - Possible values: 0 (off), 1 (on)
    - Default: 0 (off)
  - SBWAITCNT:
    - Number of frames to wait in between instructions when "SBWAIT" is set to 1.
    - Possible values: all valid WAIT values.
    - Default: 1
  - SBINDENT:
    - Indent code within WHILE and REPEAT loops, as well as IF-THEN statements.
    - Possible values: 0 (off), 1 (on)
    - Default: 1 (on)
  - SBNEWLINES:
    - Add new lines between converted instructions.
    - Possible values: 0 (off), 1 (on)
    - Default: 1 (on)

Changelog:
- v2.2.2 (SB3 Only)
  - Final SmileBASIC 3 release.
  - Options are now in a separate file named -BF2SBOPTS.PRG.
  - Changed the way the BITWIDTH option works.
  - Optimized code structure so that all variables are defined at the beginning of the program.
  - Optimized various parts of code to be shorter.
- v2.2.1.1 (SB4 Only)
  - NOTE: This update was not released via the new public key.
  - Added warnings to move to the newer version of BF2SB via the new public key.
- v2.2.1:
  - Fixed a few bugs and typos.
  - Optimized certain parts of code for SmileBASIC 4.
- v2.2 (SB3 only):
  - Heavily improved conversion process. Its code is now much more readable, and the process itself is a lot faster.
  - Improved how converted code checks for memory overflows or underflows.
  - Added option "SIGNEDINT" for choosing whether to use unsigned or signed integers.
  - Added option "SBMEMOF" to choose what to do when an overflow or an underflow is reached (wrap or abort).
  - Added option "SBCHR13" for handling character code 13 newlines.
  - Added options "SBWAIT" and "SBWAITCNT" for choosing whether to wait a certain amount of time between converted commands and how long to wait, respectively.
  - Moved option descriptions to this document.
  - Replaced "BITWIDTH.B" with "CELLWIDTH.B", which is a lot smaller in size.
- v2.1:
  - Added new option "SBINPUT" for choosing how to recieve input (from string or wait for input).
  - Added new option "SBNEWLINE" for adding newlines in between converted instructions in order to make them easier to read.
  - Correctly capitalized "brainf**k."
  - Fixed several bugs and typos.
- v2.0.1 (SB4 only):
  - Compressed all files using the SmileBASIC 4 file format.
- v2.0:
  - Brainf**k code can now be optimized (on by default).
  - Updated converted code optimization to support more sets of code.
  - Heavily improved indentation. It is now done alongside the conversion process and is a lot faster.
  - Added brainf**k code optimization option ("OPTIMIZE").
  - Added memory size option ("MEMSIZE").
  - Added bit width option ("BITWIDTH").
  - Added extra comments option ("SBCOMMENTS").
  - Added converted code optimization option ("SBOPTIMIZE").
  - Added fail-safes for options.
  - Included "BITWIDTH.B".
  - Updated code formatting and comments.
  - Made separate file "-README.TXT" for more information about BF2SB.
- v1.1.1 (SB3 only):
  - Added variable for enabling/disabling indentation for WHILE loops.
  - Added changelog to converter code.
  - Added BF2SB version in converted brainf**k code.
  - Fixed typos in some comments in the converter code.
- v1.1 (SB3 only):
  - First SmileBASIC 3 release.
  - Added indentation for WHILE loops.
  - BF2SB version is now displayed during the conversion process.
  - Added more comments in both the converter code and converted brainf**k code.
- v1.0 (SB4 only):
  - First SmileBASIC 4 release.
  - Initial release.
