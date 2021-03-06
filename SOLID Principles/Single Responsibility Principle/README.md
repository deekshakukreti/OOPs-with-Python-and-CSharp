
# Single Responsibility Principle

There should not be more then one reason for a class to change. A class should be responsible for a single part of the functionality.

For example, you should have a separate class that handles errors and not handle the errors within a class that should be doing something else. The second most common violation of the single responsibility principle is when the presentation logic in the class method. The third most common violation of the single responsibility principle is when the class or method becomes responsible for handling the persistence layers logic. The persistence layer could be anything, it could be a file or it could be a database.  We have an array of employees and we want to give them a raise of some percentage, that's what this method should be responsible for. This method should not be responsible for writing those employees to the persistence layer, in this case to a file. So this part of the functionality belongs either to another function or to another class entirely.

It is the concept that instructs developers to write code that has only one reason to change. If suppose class has more then one reason to change, then it will have multiple responsibilities. So class with more then one responsibility can be broken down to small classes, each of which will have one responsibility and one reason to change.

It is a concept of a class doing one single thing at a time and not trying to do more then it. It is also referred as high cohesion.


Why is it important to seperate two responsibilitites into two classes ?
Because it is easy to maintain code as responsibility is an axis of change. If the requirement changes, the change will be implemented by change in responsibility among the classes. If a class will perform multiple responsibilitites, then there will be multiple changes in the class.

With more then one responsibility in class, the classes are coupled. If the classes are coupled, then changes in one responsility might break the other responsibility. This design leads to fragile design that breaks in unexpected ways when changed.

For example two different applications Computational Geometry Application and Graphical Application uses a Square class which have Draw method and Area method. The Computational Geometry application does not draw square on the screen but the Graphical application does draw square on the screen.

This design violates the SRP. This is because, it has more then one responsibility in the class. Secondly, if a change to the Graphical Application causes the Square to
change for some reason, that change may force us to rebuild, retest, and redeploy the Computational Geometry Application. The application will break if it is not done.

Below is the SPR followed design class structure :

<p align="center">
  <img width="460" height="300" src="https://github.com/deekshakukreti/Images/blob/main/spr.png">
</p>

With the help of delegation and abstraction, the class which contain more then one responsibilitites could delegate responsibilities to other classes. 
