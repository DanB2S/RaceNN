# Race Cars with Neural Network v1.0.0

  This is a program, made in C++ with SDL2, for training a neural network in a mini-game of racing cars. 
  
  It works by generation one thousand random cars with one neural network each, driving them into a track and select the best by a genetic algorithm. For each epoch, the top ten cars are selected and applied to a crossover algorithm with some mutations, therefor, generation 990 new cars. This process is repeat until a satisfying car born.

## Requirements

  For this min-game work, we need 2 files and an image:
  - The first file is located at `data/track/`. It's starts with two numbers that represent the start position X and Y of the track. Beware that the car always starts for the right. After that, there's a matrix of 0 and 1, where 1 represents road and 0 off-road in the track. This file can be generated and modified, if you want to generate your own track.
  - The second file is located at `data/track_score/`. It's represent the scores lines that works as a checkpoint for the car, it's mandatory to evaluate the car's neural networks. It's start with the numbers of checkpoint lines. After, those lines represented as two points in the track.
  - The third is an image, just for visual representation of the track, that can be useful for generating the 2 files above.

## Start settings

  For easy configuration of all program settings, I've created a start windows that works as a settings tab.

<p align="left">
  <img src="https://github.com/DanB2S/RaceNN/assets/77987747/32a5b201-37a5-42a3-913b-cdc188f8be04" width="560" title="Start Window">
</p>

  It's preview the map that can be chosen, and the button `only road`, where you can change the map to show only the roads. At the right, you can choose between `Train Population`, `Single Car Run` or `Player Drive`.
  - With `Train Population` you can train the neural network with all 1000 cars. With the button `Save weight`, you can choose save the weights of the best car and the button `With Treined Weight`, it will read the weight of the best car saved previously and load it in the first car.
  - With `Single Car Run` you can see the best car saved running alone.
  - With `Player Drive` you can drive the car by yourself. Keys: `W A S D` and `delete` to reset.
  - The best part of those last two options, is that you can see the car's sensors, and how they work, as shown in the image below.

<p align="left">
  <img src="https://github.com/DanB2S/RaceNN/assets/77987747/0026cd03-65fd-4236-a724-f840ae9d47c7" width="120" title="Car">
</p>

## Running

  As soon as you press `GO`, the cars will start driving.
  
<p align="left">
  <img src="https://github.com/DanB2S/RaceNN/assets/77987747/6167935f-e9c3-4a23-ae5d-1e5bc6678b18" width="150" title="Running">
</p>

  As you can see on the right, there's a visual representation of the neural network of the best car:
  - In the left the `Input Layer` (eight directions, distance from next checkpoint and speed of the car), in the middle the `Hidden Layer` (10 neurons) and at right the `Output Layer` (throttle, right, left and brake). 
  - The lines represent the weights: green for positive weights, blue for negative and black for neutral. 
  - Some useful information as: `Score` of the best car, `Best Score` from all epochs, `Lap` of the best car, `Generation` as epoch of the cars and `Time` a timer that eliminate the slow cars.

<p align="left">
  <img src="https://github.com/DanB2S/RaceNN/assets/77987747/5cae1e8d-494b-4edc-a3de-0c54c159d982" width="220" title="Running">
</p>

## Before you go

  - Beware that this form of neural network training is pure random, in other works, will depend on your luck. If you find yourself in a Local Best, where you can't evolve, don't be afraid to start again. In tests, the cars can take from 15 epochs to 200 to make a turn.
  - It took one year to finish a decent version of this project, so the code is really messy. I'm trying to fix it, but I can't guarantee.
  - `Sometimes it may crash`. This is very random, and I can't find why. Maybe someday.

  Feel free to send me a message.

## Creator

  - Daniel (@DanB2S)






  
