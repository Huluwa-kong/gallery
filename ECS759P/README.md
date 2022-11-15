# ECS759P 
## Artificial Intelligence: Coursework 1

Due date: 16 Nov 2022 at 10.00 am



1 Introduction
The coursework is composed of two parts, involving coding exercises:
• Agenda-based search: 60% + 2% extra
• Genetic algorithm: 40%
The total mark will be capped to 100%.
2 Agenda-based Search
This part of the coursework is intended to help you understand how the agenda-based search works
and to give you practice in its implementation.
You task is to build an AI route  nder using agenda-based search mechanism. You are given a data  le
(tubedata.csv) in CSV format with the London Tube map (which is not necessarily to be up-to-date
and complete). The Tube map is de ned in terms of a logical relation Tube \step". If you open the
data  le with any text editor, you will see the content of the  le as:
"Harrow & Wealdstone", "Kenton", "Bakerloo", 3, "5", "0"
"Kenton", "South Kenton", "Bakerloo", 2, "4", "0"
     
"Bank/Monument", "Waterloo", "Waterloo & City", 4, "1", "0"
Each row in the CSV  le represents a Tube \step" and is in the following format:
[StartingStation], [EndingStation], [TubeLine], [AverageTimeTaken], [MainZone],
