Notes:

* what do these images have in common?
    * images of digi-comp II and also a woman from NASA in the 50s and also a laptop
    * they have all been called "computers" at one time.
* personal background: I stumbled across one of these in the Stata Center at MIT and became completely absorbed with it, tinkering until I felt I understood how it worked.
* educational computer (what we would now call a calculator), built in 1960s
* analogous to electronic digital computer
    * bigger and slower, so you can see what's happening
    * logic gates are chained together in such a way that what happens at each gate affects what happens at the next gate (Markov process??)
* what it can do:
    1. Count out a specified number of balls.
    2. Count in binary arithmetic.
    3. Add.
    4. Multiply.
    5. Multiply and add.
    6. Obtain either the "1's" or '2's" complement,
    7. Subtract.
    8. Divide.
    9. Zero or clear.
    10. Overflow.
    11. Halt.
* what's up with binary?
    * binary can be confusing at first because when we learn math in school, we take our particular number system for granted, assuming it's just how numbers are, instead of one of many possible systems.
    * breaking that down:
        * start by imagining a number system in which you had a unique character to represent every single number. so like 1, 2, 3,... [type out numbers and symbols with keyboard].
        * but that wouldn't be very useful because you wouldn't be able to represent arbitrarily large numbers, and you wouldn't be able to do math.
        * the number system you are familiar with uses what's called base 10. what that means is that our system has unique characters for ten different numbers: 0 through 9. so if we're counting up from 0, we use a unique symbol for each number up through 9.
        * after that, we start repeating ourselves, building the subsequent number, 10, out of symbols we've already used: 0 and 1.
        * we use the concept of digits in different places to make sure each number has a unique representation, even though we're reusing the same symbols over and over.
        * 10 is represented by a 1 in the tens place and a 0 in the 1s place. 10 is literally one 10 and 0 ones. 11 is 1 ten and 1 one. 25 is 2 tens and 5 ones. 368 is three hundreds, six tens, and 8 ones. and so on.
        * in grade school you probably learned about [*********talk about carrying************]
        * but what if we didn't have the symbol for 9? what if we only had symbols for 0 through 8? we could actually make a number system that was base-9. we would use unique symbols up through the number 8, then start repeating ourselves. in this system, this [***10******] would be used to represent the number 9, and this [***11***] the number 10. This [***28***] would be two nine and eight ones; in other words, 26. the same carrying logic that learn in base 10 would apply in base 9, only we would carry every time we wanted to increment a digit that already had a value of 8.
        * but let's get back to the question of binary. binary is just another number system that uses a different base. specifically, it uses base 2. that means we have only two unique symbols to work with, 0 and 1.
        * to represent the number 2, then, we could need multiple digits. This [***10***] is what the number 2 looks like in binary.
        * [***talk about the 1s, 2s, 4s, 8s, etc. places***]



footage to use:
A
https://shop.evilmadscientist.com/productsmenu/375 OR https://www.youtube.com/watch?v=_tZdE-3nR3w&t=5s

B
https://www.youtube.com/watch?v=fLuvopVjAWg

A step-by-step:
at 1:00, the example of multiplying 5 by 9 starts.
1. at 1:26, the start lever is pulled, releasing a ball.
2. because "multiply" is set to on, the ball is directed to the left.
3. as it goes, it reaches its first fork, where it takes a left because of the orientation of the switch. in the process, it flips that switch to the left, such that the second ball to reach that fork will go to the right. but of course in so doing, that second ball will flip the switch to the right, sending the third ball to the left. and so on. each time a ball reaches this fork, it will go the opposite direction as its predecessor.
4. after the first ball passes through the first fork, it reaches another fork, where once again it is directed towards the left, in the process flipping that switch such that the next ball to reach that fork will go to the right. of course, only every other ball will reach that fork to begin with, since the previous fork is only sending every other ball in that direction. so that means the first, third, fifth, and so on ball will reach this fork, and every other one of those balls – meaning the first, the fifth, the ninth, and so on, will go left at this fork. in other words, a quarter of the balls will end up going left at both forks, and a quarter will go left and then right.
5. the balls that take a right at the first fork will also run into another alternating fork, meaning a quarter of the balls will go right and then left, and a quarter will go right and then right.
6. but why does this matter? well, this process ends up directing each ball along one of four paths, where it can accomplish some step in the calculation. what's more, the balls traverse these paths in the same order, over and over again. the first ball will take the left-left path, the second ball will take the right-left path, the third ball will take the left-right path, and the fourth ball will take the right-right path. then it repeats. you can think of it as a cycle. we're going to talk later about what happens during each cycle and why.
7. to get there, we have to first talk about each of those paths. the left-right path – that is, when the ball takes a left at the first fork, then a right at the second, directs the ball along this path, where, because of the configuration of the memory, the ball just falls into a hole without changing anything else on the board. from there it takes a tunnel path down to the bottom, where it presses the start lever, releasing the next ball.
8. similarly, the right-left path, where the ball takes a right at the first fork, then a left at the second, leads the ball to another hole, again without it changing anything else on the board. we'll come back to the purpose of these paths later. (maybe say the next two sections later?)
    9. so when the ball takes one of those two paths, the only contribution it's making to the calculation is to reconfigure these forks, so that the next ball can take one of the other two paths.
    10. notice that if the memory register were configured differently – in other words, if we were multiplying 5 by a different number – then that would change these paths. for example, if this ___ were set at 1 instead of 0, this path would send the ball into the count register.
11. speaking of the count register, let's talk about what's happening on the right-right path. if the ball takes a right and then another right, it enters the count register here, and as it passes the top switch, it flips it from 0 to 1. in the process, it gets redirected off to the right, where it makes its way down to the bottom and presses the start lever, thereby releasing another ball.
12. but notice that if another ball were to make its way along the right right path and enter the count register, it would take a left at this top switch, flipping that switch back to 0 in the process, and then make its way to the second switch in the count register, where it would be directed to the right and out of the way, in the process flipping that switch from 0 to 1.
13. and this pattern gets repeated. each time a ball comes through the count register, it flips the top switch from either 0 to 1 or 1 to 0, and if it flips it to a 0, it then goes on to flip the next switch from 0 to 1 or from 1 to 0. and if this second switch is being flipped from 1 to 0, then the ball gets directed onto the path of the third switch, and so on.
14. so what's going on here? well, it looks an awful lot like... counting, right? the count register starts with all seven switches pointing toward 0, for a total of 0000000, or, more concisely, 0. the first time a ball comes through, it flips the first switch to 1, bringing the count to 0000001, or 1. the second time a ball comes through, it flips the first switch to 0 and carries the 1, switching the second switch to 1. this leaves us with 0000010, or 2. 

    later: in binary, carrying happens every time you want to increment the value of a digit that is already set to 1. (remember, this is analogous to carrying every time you want to increment a digit that is already set to 9 in the base 10 system).
15. this pattern will continue. every time a ball comes through the right-right path, it will increment the total in the accumulator register by 1. remember, because it will become relevant shortly, that every fourth ball travels down the right-right path.
16. ok, so that's what' happening in the right-right path. what about the other path that does something other than reconfigure these initial logic gates, the left-left path?
17. the left-left path is the most complicated path in this particular calculation because the balls that travel along it actually do two separate things.
18. the first thing is something in this multiplier register, so let's look at that first.
19. notice that the multiplier register is initially set at 101, or 5. (mirrored) the first time a ball comes through, it will hit the top switch and get directed off to the right, flipping the switch to 0 in the process. the second time a ball comes through, it will flip the first switch back to 1 as it's directed to the left, where it then travels to the second switch, flipping that switch to 1 and getting directed to the third switch, which it will flip to 0. are you noticing the pattern here? something similar is happening here in the multiplier register to what was happening in the accumulator register. we're counting, only here it's happening in reverse. each time a ball comes through, we're decrementing the count in the multiplier register by 1. it starts at 101, or 5. after the first ball comes through, it reads 100, or 4. after the second ball, it's 011, or 3, and so on.
20. eventually, if enough balls pass through the multiplier register, its value will be equal to 0, with all three switches pointing to the right. take a moment to think about what happens at that point. we'll come back to why that's significant in a bit.
21. I mentioned earlier that a ball traveling along the left-left path performs two actions. the first, we've seen, is to decrement the value in the multiplier registry. so what's the second?
22. well, you can see that after leaving the multiplier register, any given ball will end up on this path. from here, it will travel down to here and enter the accumulator register. once there, it will follow a pattern we should be starting to find familiar. if the first switch that it hits is pointing to 0, it will flip that switch to 1 and escape the accumulator register. if the first switch that it hits is set to 1, then it will flip it to 0 and carry the 1 to the next switch. and so on. we're counting again, right?
23. well sort of. notice that we're starting not at the 1's switch at the top of the accumulator register, but at this switch labeled A4. to understanding how that changes what's happening, consider how flipping the A4 from 0 to 1 changes the value in the accumulator register. if the accumulator register were set to 0, flipping A4 from 0 to 1 would change its value to 1000, also known as 8. this A4, the fourth digit in a binary number, is the 8's digit. in the same way that incrementing the 10's digit in decimal numbers increases the number's value by 10, incrementing the 8s digit in binary increases the number's value by 8. and because any ball that enters the accumulator at this digit is skipping all of the digits that come before, each ball that follows this path will increase the value in the accumulator by 8.
24. ok, so now we know that each ball that take the left-left path decrements the multiplier register by 1 and increments the accumulator register (or our total) by 8.
25. we also know that the right-right path increments our accumulator register, or toal, by 1, and that the left-right and right-left paths come are traversed in between in order to reconfigure our initial logic gates.
26. we also know that these paths are traversed in a cycle. left-left, followed by right-left, followed by left-right, followed by right-right.
27. so if we put all this knowledge together, we'll realize that each time we go through one of these cycles, the accumulator register is incremented by both 1 and 8, for a total of 9, AND the multiplier register is decremented by 1.
28. remember when I asked you to think about what would happen once the value of the multiplier register got down to 0? well at that point, with all the multiplier register switches pointing to 0, the ball will have a clear path through the multiplier register, without getting directed toward the accumulator register at all. it will pass right through to this winding path on the far left. this path takes the ball all the way down to the well at the bottom without sending it through the path of the start lever. that means this ball will be the last ball of our calculation.
29. notice that at this point, the cycle has repeated itself a total of 5 times. that's a total of 5 cycles, each of which has incremented our accumulator register by 9. sound familiar? that's our multiplication problem – 5 times 9.
30. looking at our accumulator register, we see that it reads 0101101, or 45, the product of 5 and 9.
31. now that we've walked through how the digi-comp II solves this multiplication problem, think through how changing the value in the memory register, say from 9 to 11, would change the calculation process. when you've figured that out, think about how you could use the digi-comp II to solve a subtraction or division problem.
32. thanks to Evil Mad Genius for letting me use their photos and footage in this tutorial. see the description for links to their pages.
33. and thank you, for watching this video.



00000 = 0
00001 = 1
00010 = 2
00011 = 3
00100 = 4
00101 = 5
00110 = 6
00111 = 7
01000 = 8
01001 = 9
01010 = 10
01011 = 11
01100 = 12
01101 = 13
01110 = 14
01111 = 15
10000 = 16


Resources consulted:

https://en.wikipedia.org/wiki/Binary_number
https://www.csail.mit.edu/news/video-how-digi-comp-ii-works
http://www.oldcomputermuseum.com/digicomp_2.html
https://shop.evilmadscientist.com/productsmenu/375
https://www.youtube.com/watch?v=fLuvopVjAWg
https://www.youtube.com/watch?v=SYi9sJkS19Q
https://en.wikipedia.org/wiki/Digi-Comp_II

virtual version?
https://connect.unity.com/p/games-virtual-digicomp-ii

coded version?
https://jamesmccaffrey.wordpress.com/2018/07/30/digi-comp-ii-simulator-program-using-python/




Questions people have:
* I've watched the video, but how does it actually work?
* What is the twos complement?
* What does it mean to clear the register?
