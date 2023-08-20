# NN-for-classification-and-regression-task

In this example I solved the combined classification and regression task by reporting both the number of showers in the event and the parameters of each shower.

Problem

The calorimeter has a multiple showers where the energy is distributed through multiple blocks. The shower centers can be anywhere in the calorimeter ( –1000 < x,y < +1000 ) and will never be outside of that. Energy from the shower that falls outside of the calorimeter however, is lost.

Each shower has three values: shower amplitude, x-coordinate of shower center, y-coordinate of shower center. So in case of 3 showers we have (amp1, X1, Y1, amp2, X2, Y2, amp3, X3, Y3). For events with fewer than 3 showers, the parameters are set to –1. So for example, for a 1 shower event the labels would be (amp1, X1, Y1, -1, -1, -1, -1, -1, -1).

The showers here are all “clean” with no noise or backgrounds.

The data comes as PNG files (8-bit greyscale) for each of the events that are stored in the relevant directory such as "train_images". For this set, there is an CSV file named "train_images.csv". The first column is just the PNG file name and the next 9 columns represent the amplitude, x, y of the three showers (in that order) in the same units as are used for the labels. For events with fewer than 3 showers, the amplitudes for the missing showers should be set to a value < 0. Any showers with an amplitude less than 0 will be considered to mean “no shower”.

The solution to this problem will consist of a single CSV file with 9 columns containing the parameters (amp, X, Y) for each of 3 showers in the event for the events in the judge.csv or judge_images.csv file. Each row in the output should correspond to the events in the judge data set, in the same order of the events there.
