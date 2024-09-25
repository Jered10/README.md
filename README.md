# Flight Data Analyzer

## Overview
The **Flight Data Analyzer** is a Java program designed to analyze flight data from a CSV file. It provides various functionalities, including finding unique airports, calculating passenger statistics, and measuring the runtime for specific operations. 

## Features
- **Find Maine Airports:** Identifies all unique airport names in the state of Maine (ME) from a list of flights.
- **Maximum Passengers:** Determines the maximum number of passengers on flights with Portland International Jetport (PWM) as the destination.
- **Full Flights Percentage:** Calculates the percentage of full flights (flights with no empty seats).
- **Average Passengers:** Computes the average number of passengers on flights from PWM to Florida (FL) for the year 2009.
- **Runtime Measurement:** Checks and measures the execution times for various operations to analyze performance.

## Structure
The project is organized into several classes, each serving a specific purpose:

- **Flight:** Represents a flight with properties such as origin, destination, passengers, seats, distance, and flight date/time.
- **Airport:** Represents an airport with properties like airport name, city, and state.
- **MyDataReader:** Handles reading flight data from a CSV file and parsing it into Flight objects.
- **MyAnalyzer:** Provides methods for analyzing flight data.
- **MyArrayList:** A custom implementation of a dynamic array list.
- **FlightComparator:** Implements sorting functionality for flights based on their origin airport names.
- **Program1 & Program2:** Demonstrates the functionalities of the program and measures execution times for sorting and analyzing flights.

## Usage
To use the program:

1. Ensure that you have a CSV file (e.g., `flights.csv`) containing the flight data.
2. Modify the file path in the code as necessary to point to your CSV file.
3. Compile and run the Java program.
