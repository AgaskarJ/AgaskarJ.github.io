# OOD-Animator
Our model has 3 interfaces: IModel, IAnimation, IShape. IModel is where one can add to,remove from, and receive a description of the current model of shapes being displayed. IAnimation has 3 functional animation techniques - scale, move, and changeColor. IShape extends IAnimation, so that each shape has the ability to animate, and holds methods to create shapes.

In our model we assume shape names are unique and will not be repeated.

--IModel--

IModel is an interface that over looks the entities, having the following methods: 

createShape - adds a shape to the arrayList of shapes currently in the model
removeShape - removes shape by name in the arrayList of shapes currently in the model
printAnimation - prints out each shape and their list of animations

--ModelImpl implements IModel--

This class defines all the methods of IModel and has a consturtor to create an Model from an ArrayList of IShapes. In the future there will probably be a contructor that works based off of user input.

--IAnimation--

The animation interface is used to keep track of the animations that are implemented. Our model supports scaling, moving, and changing color.

move
scale
changeColor

--IShape extends IAnimation--

IShape is an interface which holds the methods of AShape and it extends IAnimation so that every shape has a list of animations it can preform.

getPosn
getColor
getWidth
getHeight
getName
getType
getAppear
getDisappear
getAnimations

--AShape implements IShape--

Abstract class for shapes. Implements all methods in IShape and IAnimation for simplification when implementing specific shapes. This allows for expansion and easy addition of shapes later on.

--Animation--

This is a class to hold the animations and their descriptions. Has a getMsgNum method to return the msg we want for the board.

--Oval extends AShape--

The class for a specific Oval shape implementation.

--Rectangle extends AShape--

The class for a specific Recatangle shape implementation.
