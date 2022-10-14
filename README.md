# intent-oriented-design
IOD focusses on the single intent a solution is suppose to cover, an application is just a composition of intents. IOD is basically DDD but as a composable set of intents. 

__Assumptions__
1. All applications can be represented as a single intent hence a single entry point
1. An intent may or may not be composed of calls to other intents (a module)
1. An intent can be represented as a single function

IOD's goal is to optimize packaging and code surface area in large applications (which most applications become). The downside to spliting the entire code base into a composition of functions is that it is hard to track,read or work with. A way to olve this is to divide all intent into code cells like jupyter did with python but the major difference here is that the order of execution is important. The order of excution will follow a downward path in teh intent dependency tree.

This way developers can pull source code for a single intent and only make changes to specific intents. CI pipelines can focus on testing specific intent set. containers can be packaged to serve more specific intents, kind like microservice that is carved out of a monolith using a packaging rule based on coupled intents.

### IOD in the DATA layer?
