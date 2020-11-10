# How the Internet Works

The internet in our lives to day is a taken-for-granted abstraction of communication between computers worldwide. Let's peel back the layers and try to understand some of the fundamental concepts that are the buildingblocks to communication. If you research this yourself, you will find protocol layers and buzzwords that may make it hard to understand at first. The goal here is to attack the problem by breaking it down into its base elements and reverse engineering it as if we were designing the internet ourselves. Hopefully, this will give you a base understanding that will allow you to better digest resources that you research for yourselves in the future. 



Let's start simple. You open your browser and type in www.google.com. In a few seconds, you see the google homepage. What just happened?

Well, before we answer that, I want you to think about what you think would have to happen. You live in a world where the internet does not exist. You want to be able to get information to your computer from a computer that Google owns that is sitting in San Fransisco just by typing in "www.google.com" into your browser. What problems must you solve? Try to think about it a little before moving on.


Ok, so here are some problems we have to solve:

1. Mapping the physical location of the computer owned by Google using the `string` "www.google.com" (in the tech world, the word `string` means a series of text characters)
2. Physically sending a request for information from your computer to the location of the Google computer
3. "Speaking" to the Google computer in a language that it understands (and that your computer will understand when it sends you a response)
4. Making sure that all of the communication between the two computers makes it to its destination
5. Turning all of the data into a visual respresentation on your screen


I think that this covers the basic problems we have to solve. Let's start by skipping a little bit ahead and focusing on step 4. 

When two humans communicate, we have to use the tools that we have in order to convey information to another human in a way that they understand. To achieve this, we have developed a set of "rules" (a.k.a. a `protocol`) that allows us to easily communicate with one another. This is done via language. Right now, because I am following the rules described by the English language, I am able to put symbols on a page that you are able to read and understand. The same must be true for computers. Instead of having the ability to speak or write, however, computers have to use the tools available to them in order to communicate. Due to the nature of the constructions of computer "brains", this must ALL be done by a series of 1s and 0s. Computers think and speak in `binary`, as they are only able to represent these two distinct values. 

You are probably thinking - well this seems impossible. But because we tell computers to follow rules with the 1s and 0s, we can do more than you might think. First of all, how do we represent numbers larger than 1? By using the `binary` number system. As humans, because of our 10 fingers, we communicate numbers in base 10. When we want to represent a number from 0-9 this is easy; each number has its own symbol. What happens though when we want to represent a number greater than 9? Well, we add extra symbols to tell the other person how many 10s already exist. The number 13 means "one ten and then three more". If the only symbols we have is 1 and 0, we can still do the same thing. The numbers 0 and 1 are represented the same as base 10, but if we want to represent something bigger than 1, we use an extra "place". For example, the number 3 in binary is `11`, meaning "one 2 plus 1 more", giving us the number 3.

|Base 10 (Decimal) | Base 2 (Binary) |
|------------------|-----------------|
|0|0|
|1|1|
|2|10|
|3|11|
|4|100|
|5|101|
|6|110|
