# Airport Security Queue Simulation

## Overview
This project simulates an airport security queue, focusing on determining the minimum number of counters needed to process all passengers on time based on flight schedules. The system reads flight data from a CSV file, filters it by state and airport, and then calculates how many counters are required to process passengers based on their arrival times.

## Project Structure
- **Airport.java**: Represents an airport with a name, city, and state.
- **Flight.java**: Represents a flight with origin, destination, flight time, passengers, seats, and distance.
- **MyDataReader.java**: Reads flight data from a CSV file and provides filtering and sorting functionality based on origin state and airport.
- **MyQueue.java**: A generic queue implementation using an ArrayList, used for processing flight data in a queue structure.
- **Program4.java**: The main class that reads flight data, processes it, and calculates the minimum number of counters required to process all passengers.
- **QueueSim.java**: Simulates the passenger processing for each hour and calculates the minimum number of counters required to ensure all passengers are processed on time.

## Class Descriptions

### 1. Airport.java
**Description**: Represents an airport with three fields: airport name, city, and state.  
**Methods**:
- `getAirportName()`: Returns the name of the airport.
- `getCity()`: Returns the city of the airport.
- `getState()`: Returns the state of the airport.
- `toString()`: Returns a string representation of the airport.

### 2. Flight.java
**Description**: Represents a flight object, including origin and destination airports, passengers, seats, flight date/time, and distance.  
**Methods**:
- `compareTo(Flight otherFlight)`: Compares flight times to allow sorting.
- Getters for origin, destination, passengers, seats, and flight date.

### 3. MyDataReader.java
**Description**: Utility class to read flight data from a CSV file, filter it by state, and sort flights by airport.  
**Methods**:
- `readFlightsFromCSV(String filePath, String originState)`: Reads flights from a CSV file, filtering by the given state.
- `FlightSorted(String airportName, MyQueue<Flight> flights)`: Filters and sorts flights by the specified airport.

### 4. MyQueue.java
**Description**: A generic queue class implemented using an ArrayList. It provides typical queue operations such as offer, poll, peek, and size.  
**Methods**:
- `offer(T input)`: Adds an element to the queue.
- `poll()`: Retrieves and removes the head of the queue.
- `peek()`: Retrieves but does not remove the head of the queue.
- `isEmpty()`: Checks if the queue is empty.
- `size()`: Returns the size of the queue.

### 5. QueueSim.java
**Description**: Simulates the passenger processing for each flight and calculates the minimum number of counters needed. It processes flights by hour and ensures all passengers are processed within the available time.  
**Methods**:
- `addToQueue(ArrayList<Flight> sortedFlights, LocalDateTime currentTime)`: Adds flights scheduled within a specific time window to the queue.
- `calculateMinCounters(ArrayList<Flight> sortedFlights)`: Calculates the minimum number of counters required to process all passengers on time.

### 6. Program4.java
**Description**: The main class that runs the simulation, reads flight data from a CSV file, and determines the minimum number of counters needed to process all passengers.  
**Methods**:
- `main(String[] args)`: Takes three command-line arguments: the path to the CSV file, the state to filter flights by, and the airport code.

## Usage
### Command-Line Arguments
The program expects the following arguments:
- **CSVFilePath**: The path to the CSV file containing flight data.
- **State**: The state code (e.g., "ME") to filter flights by origin.
- **AirportCode**: The airport code (e.g., "PWM") to further filter the flights.

**Example command**:
```bash
java Program4 flights.csv ME PWM
