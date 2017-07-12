# RedditClone
A Digg / Reddit clone with upvote and downvotes

-  Clean, Simple and Minimalist design
-  Follows MVP architectural pattern
-  Uses Dagger2 for DI
-  Use Gradle to build, jCenter/Maven Central for dependencies (no .jar dependencies)

Functionality present

- Maintained a list of topics and its upvotes/downvotes
- Allow the user to submit topics (not exceeding 255 characters)
- Allow the user to upvote or downvote a topic. user may upvote or downvote the same topic multiple times.
- Always return a list of top 20 topics (sorted by upvotes, descending) on the homepage
- In memory data structure to keep data
- Allow the user to Edit topics after created
- Nice, simple and easy to operate user interface

Implementation

- I created a Plain Old Java Class Forum to store Topic data and using setter and getter methods to save and retreive data.

- In-memory data structure: For this, I implemented the Application class which is instantiated before any other class when the process for the
 application/package is created. The application object also runs at least as long as another component of the application runs.

 I therefore managed my Forum class which stores Topic details in the Application class.

 - Using Dagger2: I implementation Dependency Injection with Dagger2 to make classes loosely coopled and organized, this also promotes logical
 abstractions of components, interfaces and their implementations.

 - Sorting the Upvotes: For this, I used the in-built Collections.sort method with Comparator, along with the Integer signsum Java function which returns
 -1, if the value is negative and zero, if the value is 0, It returns 1 if the value is positive.

