# PubSubServerExercise - Demo Implementation

[You can view requirements for this task here](https://github.com/devsitecore/PubSubServerExercise/blob/master/Requirements.md)

## Opening the solution:
Once you download the files, you can open the solution in Visual Studio 2015 or above.

Visual Studio solution file path: \PubSubServerExercise\Source\PubSubSample.sln

You can compile the application, it should install the packages from NuGet during compilation. Once solution is compiled, it will produce 3 executables (Windows form applications)

**PubSub Server**
\PubSubServerExercise\Source\PubSubSample.PubSubServer.Host\bin\PubSubSample.PubSubServer.Host.exe

**Publisher**
\PubSubServerExercise\Source\PubSubSample.Publisher.Host\bin\PubSubSample.Publisher.Host.exe

**Subscriber**
\PubSubServerExercise\Source\PubSubSample.Subscriber.Host\bin\PubSubSample.Subscriber.Host.exe
  
## Testing the output:
 To view the run-time behaviour of the solution, you can click the pre-created bat files located at the path `\PubSubServerExercise\Source`.
 
  - **0_Launcher.bat** - Clicking this will launch one instance of PubSubServer, Publisher and the Subscriber
  - **1_AdditionalSubscriber.bat** - For multiple scribers testing, you can open this bat file to open multiple instances of subscribers
  - **2_AdditionalPublisher.bat** - To launch multiple publishers, you can use this bat file

### PubSubServer
When `0_Launcher.bat` is launched, it will open a Windows form application that will host services for subscribers and publishers. The window form will remain open and different messages will be displayed as different operations are performed. When you launch this first time, it might ask you for permissions based on your OS.

![PubSubServer](https://github.com/devsitecore/PubSubServerExercise/raw/master/Documentation/pubsub-server.png?raw=true)

PubSubServer is the centeral component of this solution. There is one way communication between Publisher and the PubSubServer, Publisher can only publish messages over to PubSubServer where each message is tagged with a topic.

There is two way communication between Subscriber and the PubSubServer, a subscriber can subscriber/un-subscriber a topic with the PubSubServer and PubSubServer will send the message based on topic as sent from Publishers. 

*You can launch one PubSubServer at a time*

### Publisher
By default one Publisher will be opened but you can open multiple Publishers too in order to fully test the functionality.

![Publisher](https://github.com/devsitecore/PubSubServerExercise/raw/master/Documentation/publisher.png?raw=true)

From each Pubsliher application, you can send messages based on a Topic. Publisher does not have any knowledge about the subscribers, it will just send the message with the topic over to PubSubServer.

*You can launch multiple publishers*

### Subscriber
By default one Subscriber will be opened but you can open multiple Subscribers too in order to fully test the functionality.

![Subscriber](https://github.com/devsitecore/PubSubServerExercise/raw/master/Documentation/subscriber.png?raw=true)

On the Subscriber application, you can subscribe to a topic. Once topic is subscribed, the subscriber will be in ready state to receive messages for the subscribed topic. You can unscriber and subscribe to a different topic too.

![Subscriber](https://github.com/devsitecore/PubSubServerExercise/raw/master/Documentation/subscriber-messages.png?raw=true)

*You can launch multiple subscribers*

## Documentation:
You can review the overall documentation about project details on the following url: 
https://github.com/devsitecore/PubSubServerExercise/wiki

 

