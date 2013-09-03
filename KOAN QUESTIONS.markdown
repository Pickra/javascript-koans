here is my gh-pages link - 
http://pickra.github.io/javascript-koans/


i really liked this exercise, aside from it bein really ruff, except the way they write the examples makes it too easy to infur the answer w/out understanding why that's the answer/how u reached that conclusion. i dono anymore if i answered these questions to my satisfaction. the process of writing them out, although it slowed me down, was helpful. and i thought id just leave them for u to puruse.




ABOUT FUNCTIONS------------------------------

	lexical scoping is crazy???
		i don't get it. the whole concept of local and global no longer exists?
	---

	line 74-- where is arguments defined? how can u have a for loop with an undefined parameter????
	---

	line 83, it statement w/ "fill me in" @ line 94--
		i intuited the answer, more because of how they wrote it than cuz i get it, but am unclear why it works.
			they made 2 functions and then made a variable called praiseSinger, which is an obj w/the property of givePraise and a property value of the appendRules function they created above.
			then they "expect" praisSinger(variable)'s property(givePraise)'s value to be 'John'. but the property value is a function. now the function does what they want it to do but it seems awfully convuluted.	
				this is an argument issue, which im still foggy on, that im missin

		ditto for line 96...
			and why is there no VAR @ the beginin of the line?? 
				i know u can create a variable without it, but they put a VAR on the variable above......
--------------------------------------------------------------------------------------------------------------------

ABOUT OBJECTS----------------------------------

	line 27, ironic, the ARRAY they r referin to is bein created @ the same time? no VAR necessary?????

	line 31, "4" is the argument, but the function is actin like a method... so by putn "4" in (), im sayn do the function 4xs. but line 27 says argument, noOfBrains, + 1. shouldnt i expect - "They are Pinky and the Brain Brain Brain Brain Brain"???????????? 
		in reality, thats how the actual song goes, that they're referencing, and that's how im reading it to go.

	line 35, "it"; but im referencing the line 47 "expect". they expect it to be "2013". I get why only becuz of context. getin lost on where it says, start @ 1970 and add 43 years.
		what i got is, start @ the currentYear variable -	
			(the problem is probly cuz i dont understand the getFullYear method cuz MDN's jargon is too thick. and what is "new" in line 36 column 26; i assume it's similar to "return" only cuz they're the same colors but don't know how to google that!)
		which is right now and subtracts 43yrs cuz calculateAge 
			(which is some vooDoo i can't seem to find the definition for, and it's a property which is actually a function tht acts like  method????!!!!!!) 
		takes the variable's "currentYear" and "birthYear"
			(which is some crazy lexical scopin bs????) 
		and finds the difference?

	line 63 what is "in"?? it's like "new", kinda? they're in the same catagory which is... what?
		i think that it loox "in" something 
			(obj, array, element, node, yada yada...)
		and sees if what ur lookn for is where ur lookn "in" and it either is (which === true) or it's not (which === false )???????

		line 84, or how about "delete"???? 
			i get that it deletes what it's attached to, but what is it???????

	line 102, what is prototype????	

	ditto, what is describe??????
----------------------------------------------------------------------------------------------------------------------------

ABOUT MUTABILITY

	line 3, what's "public"?

	line 10, what's a "constructed property"?? a constructor?????
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
	is the below right??????
		a constructor is a parent obj that u can create other objs from. if ur parent has kids, the kids r like the parent. they have the same properties and a new property(s). u have a Table obj, it is made out of some kind of material and has 4 legs. then u can create a new variable/obj that builds off of the Table parent obj. U make a new obj called MetalTable. the MetalTable has a diff property value than Table, but MetalTable still has the parent obj properties; it's made out of some kind of material and has 4 legs.

		a prototype creates methods(and or properties) that interact with the obj (that u made the method/property for), and any other objs that inherit that obj's properties(parent child scenario). if the parent obj is Table, the children objs r woodTable, metalTable, buttTable, etc... so u have an obj, Table. u make a method just for the obj(Table) which is .burn.... u now have to create the function that .burn is representing. so now every table can apply the .burn method. ditto for the properties.
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


	line 42 "it", is what im talkn bout
		they make a function called "Person" w/2 arguments(firstname, lastname). then inside that function they make a variable that uses those arguments to define itself. then they make 3 more functions(line 47-49), inside the 1st function, again using the args to define themselves.	
		
		then they make a constructor obj(aPerson, line 51), which is based off the 1st function(Person, line 43) and they give it property values that reference the functions on lines 47-49. now becuz constructor args r "private"(????????), the fact that they then redefine the constructor's properties/values(line 53-55) don't matter when u get to line 57-59.

		@ line 61, they create a function(getFullName) for the constructor(aPerson) which uses the args from line 43, which reference the properties @ line 53-55...

		is the above right? have i lost my mind?????? 

	line 51-55
		i don't get how u create a constructor, which is an obj, and define property values w/out makn a function or @ least wrapn it all in {}s. is this just how the constructor operates??? willy nilly????
-----------------------------------------------------------------------------------------------------------

ABOUT HIGHER ORDER FUNCTIONS

	in reference to http://documentcloud.github.io/underscore/   ------------  filter definition
		var evens = _.filter([1, 2, 3, 4, 5, 6], function(num){ return num % 2 == 0; });
			i get that { return num % 2 == 0; } return numbers divisible by 2. 
			it loox like it says - return numbers, that when divided by 2 equal 0
				what am i missin????

	ditto -----------  reduce definition
		what is "iterator"???? like in a "for loop"/forEach????
			on line 30 column 70, of higher order functions, the "iterator" is x????
		and what is "The iterator is passed four arguments"????
			if it said, "the iterator passes four arguments", i would understand that. but "The iterator is passed four arguments" is crap

	line 32, they expect it to b 6 cuz _.reduce "boils down a list of values into a single value" by adding all the objs in the array together?
		i know that's not right, but i can't see another solutions

	startn @ line 37, they create an array called numbers, and a variable called msg(which is an empty string), and a function that says - 
		msg(empty string) concatenates with isEven(function)'s argument(item) and divides that by 2, and all that equals 0.
		line 43, the function(isEven) is iterating(forEach), the array(numbers).
		line 45, expect empty array to glue together the results from the function(isEven). 1%2 dont equal 0 so thats false, 2%2 does equal 0 so that's true, and 3%2 don't equal 0 so that's false. 
			so 45:26 is "falsetruefalse"... right?

	line 76, i get what flaten is doin in this instance, but could use a better definition than what's on underscore's github, just sayn
-----------------------------------------------------------------------------------------------------------------------------------------

ABOUT INHERITENCE

	.call makes arguments into methods using "this"???

	lines 28, 32, 36, 37, 41: it seems like they take a waaaaaaay convluted trip to get to the answer. what seems more likely is im missin the point of ".call", or the subtlties of how it works. again the "underscore definition sux" and the answer is too easily infered. definitley misin how it worx.

	line 70, is callin the method(doTrick, line 56) on new Gonzo, line 66?

	line 74, is callin the method(answerNanny, line 5) from the parent obj (Muppet, line 1) on the new Gonzo(line 66)?

-----------------------------------------------------------------------------------------------------------------------------------------

about applying what we have learnt

	i have 1 more problem to solve. it's 10:30 monday night. ima do it in some parallel universe and then communicate with "this" alternate version of me telepathicly thru space and time. then he'll get a voodoo priest to make a gist that i can access via a dimensional rift. cuz the internets can do that kinda thing, right?










