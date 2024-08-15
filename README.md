# self_driving

The project “Self-Driving Car” is a simulation model where a road network is populated with cars all moving in same direction at a fixed speed in a three-lane road. The user inputs ‘n’ no. of cars moving at a variable speed in random direction. The primary objective is to optimize the navigation of a designated faster car amidst the traffic. To achieve this, the stimulation uses neural networks, machine learning algorithms to determine the fastest and the best route.
The simulation is visualized using an HTML interface that provides a clear and interactive display of the moving vehicles. The interface includes two essential icons: one for saving the simulation data and another for resetting the simulation. This user-friendly feature allows for efficient data management and repeated experimentation.
The stimulation has sensors on all cars which shows the best car of all the other ‘n’ cars. If the car passes the first barrier, the user can save the data for the car using the save icon. When the user run’s it again the stimulation uses ML to save the data from previous run and now the ‘n’ cars follow the previous best car. After which the ‘n’ cars move in random direction again and the sensors help us to identify the best car. The user gets an option to save the data of the best car. After the user finds the best car that crosses all the barriers the user saves it data and all the other cars now use the best car data to move in stimulation. The neural network is trained to predict the best possible routes for the faster car, adapting to the random movements of other cars on the road. The neural network is used to change the lane, increase or decrease the speed.
This approach ensures the faster car can progress forward by selecting the most efficient paths, akin to overcoming hurdles on the road to success. The project demonstrates the practical integration of AI in traffic simulation, providing insights into route optimization and real-time decision-making processes. The findings have significant implications for the development of autonomous vehicle systems, showcasing how AI can enhance traffic flow and vehicle performance in complex scenarios.

In the main neural network, I used feedforward algorithm, to detect the obstacles, and mutate algorithm helps to tell car in which direction it has to move, either right or left, here the sensors give the info to the car where the mutate algo, works and change the direction accordingly. 

I use Lerp and poly intersect algo to determine damage to the car, like when the obstacles come or there is any border there, and it got crashed, then this algo helps to show, whether it is damaged or not. 
I use 3 layers of the neural network, 1st sensors layer, 2nd hidden layer, and 3rd main direction layer. 
first I designed the car, and its damage protocol, and then I created the controls, using a keyboard listener, and one key design algo to use the control.   

then I designed the road for the car and used the translate function to just the camera, as car movies upward road will also move up. 

Then I designed the sensors, in which I gave 2 entities as an obstacle 1 is road border and the other is traffic(í named them as “dummy”).
After that, I made the visualizer, which helped to show how the neural network works. 
Then I added the save and delete button, which saves the data of the best car(which I named “best brain”) as I said earlier, there will be the random motions of the car, and between them, there will be the cars, which will perform best, I trained the neural network by saving it’s data. 

