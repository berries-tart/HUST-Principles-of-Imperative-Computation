Programming 6 (Peg Solitare)

Files you won't modify:
   lib/peg-util.c0 - utilities for reading and printing boards
   lib/ht.c0       - Hash tables (their use is optional)
   lib/stacks.c0   - Stacks
   peg-test.c0     - testing code, to verify solutions
   peg-main.c0     - main function, to read in boards and call solver

Code to fill in:
   peg-client.c0   - Client side implementation for stacks and hash tables
   peg1.c0         - Peg solitaire, no backtracking
   peg2.c0         - Peg solitaire, with backtracking 
   peg3.c0         - Peg solitaire, with backtracking and hashtables (Bonus)

Data:
   german.txt      - A trivial-to-solve board
   english.txt     - A board that you may be able to solve with peg2.c0 if 
                     you pick a very good move selection strategy (see 
                     Appendix A)
   french1.txt     - A difficult-to-solve board (but one with a solution)
   french2.txt     - A difficult-to-solve board (but one with a solution)
   french3.txt     - A difficult-to-solve-board (but one with a solution)

==========================================================

Compiling and running on the german board with -d:
   % cc0 -d -w -o peg1 peg-client.c0 lib/*.c0 peg1.c0 peg-main.c0
   % ./peg1 german.txt

   % cc0 -d -w -o peg2 peg-client.c0 lib/*.c0 peg2.c0 peg-main.c0
   % ./peg2 german.txt

   % cc0 -d -w -o peg3 peg-client.c0 lib/*.c0 peg3.c0 peg-main.c0
   % ./peg3 german.txt

Compiling and running on the english board. These direction give you
the fastest possible code, but use at your own risk!
   % cc0 -w -o peg2 -r unsafe -c-O2 peg-client.c0 lib/*.c0 peg2.c0 peg-main.c0
   % ./peg2 english.txt

   % cc0 -w -o peg3 -r unsafe -c-O2 peg-client.c0 lib/*.c0 peg3.c0 peg-main.c0
   % ./peg3 english.txt

==========================================================

Submitting with Andrew handin script:
   % handin hw6 peg-client.c0 peg1.c0 peg2.c0 peg3.c0
 
Creating a tarball to submit with Autolab web interface:
   % tar -czvf hw6sol.tgz peg-client.c0 peg1.c0 peg2.c0 peg3.c0

On autolab: https://autolab.cs.cmu.edu/15122-f13/peg
