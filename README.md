# streaming-04-multiple-consumers
# Samantha Cress 2/6/2023

> Use RabbitMQ to distribute tasks to multiple workers

One process will create task messages. Multiple worker processes will share the work. 


## Before You Begin

1. Fork this starter repo into your GitHub.
1. Clone your repo down to your machine.
1. View / Command Palette - then Python: Select Interpreter
1. Select your conda environment. 

## Read

1. Read the [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)
1. Read the code and comments in this repo.

## RabbitMQ Admin 

RabbitMQ comes with an admin panel. When you run the task emitter, reply y to open it. 

(Python makes it easy to open a web page - see the code to learn how.)

## Execute the Producer

1. Run emitter_of_tasks.py (say y to monitor RabbitMQ queues)

Explore the RabbitMQ website.

## Execute a Consumer / Worker

1. Run listening_worker.py

Will it terminate on its own? How do you know? ## No, that is why we have the option to press CTRL C to terminate. 

## Ready for Work

1. Use your emitter_of_tasks to produce more task messages.

## Start Another Listening Worker 

1. Use your listening_worker.py script to launch a second worker. 

Follow the tutorial. 
Add multiple tasks (e.g. First message, Second message, etc.)
How are tasks distributed? Each worker appears to recieve eveyother task. 
Monitor the windows with at least two workers. 
Which worker gets which tasks? Worker 1 get tasks 1 and 3, and worker 2 gets tasks 3 and 4. 


## Reference

- [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)

## Steps for version 3:
1. Six tasks were added to the tasks csv
2. This code it based on version two but code it added to read from csv file 
3. The emitter sends tasks every two seconds to multiple workers. 
4. Multiple workers split the work load of reading from csv and recieve five tasks each. 
5. To run: run the worker version 3 file twice (creating two workers) then run emiiter version 3 to send tasks the from the tasks file. 

## Screenshots


Version 3:
![1 producer 2 consumers](https://user-images.githubusercontent.com/111606778/217388444-9ea52582-5538-4e47-8dbc-602d3634f4b7.png)

Version 1:
![v1](https://user-images.githubusercontent.com/111606778/217388520-b47a42ff-b92f-40f0-8f82-cd42694227c7.png)

Version 2: 
![v2](https://user-images.githubusercontent.com/111606778/217388554-37944642-cf2c-4398-86d2-302114fbc180.png)

