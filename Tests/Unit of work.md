A **unit of work** is the sum of actions that take place between the invocation of a public method in the system and a single noticeable end result by a test of that system. A noticeable end result can be observed without looking at the internal state of the system and only through its public APIs and behavior. 
An **end result** is any of the following: 
- The invoked public method returns a value (a function that’s not void). 
- There’s a noticeable change to the state or behavior of the system before and after invocation that can be determined without interrogating private state. (Examples: the system can log in a previously nonexistent user, or the system’s properties change if the system is a state machine.) 
- There’s a callout to a third-party system over which the test has no control, and that third-party system doesn’t return any value, or any return value from that system is ignored. (Example: calling a third-party logging system that was not written by you and you don’t have the source to.)

#unitTest 