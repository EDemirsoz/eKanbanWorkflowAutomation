
# eKanban Workflow Automation

This project is a database-backed simulation that supports and tests a simple electronic Kanban solution for a manufacturer that builds fog lamp assemblies for automobiles. The goal of the solution is to automate the workflow and minimize the time it takes to assemble the fog lamps.

##  Disclaimer
The project available in this repository is an academic project and is not intended to be publicly available since it is related to academic coursework, and there is a potential for academic misconduct if it is used improperly. Therefore, only a video recording of the project is available for viewing.

If you would like to request access to code base and additional materials related to this project, please contact me directly and make your request. Please note that access to any additional materials will be granted solely at my discretion and only for legitimate educational or research purposes.

By accessing the video recording of this project, you acknowledge and agree that you will not use it for any unauthorized or unethical purposes, and that any misuse of the project may result in serious consequences, including academic penalties and disciplinary action.
## Tech Stack
- Microsoft SQL Server
- C#
- .NET Framework
- Microsoft Visual Studio


## Requirements
- Windows operating system
- Visual Studio IDE installed
- .NET Framework 4.7.2 or later installed
- SQL Server database with COVID-19 data
- COVID-19 data in a .csv file format

## Run Locally
	1. Clone the repository to your local machine
	2. Open the solution file in Visual Studio
	3. Update the connection string in the App.config file to point to your SQL Server instance
	4. Run the SQL script to create the database schema and populate it with sample data
	5. Build and run the C# programs to start the simulation and visualize the assembly line

## Database Schema
The database schema includes the following tables:

- AssemblyStations: contains information about each assembly station, such as its ID and name
- BinCards: contains information about each Kanban bin card, such as its ID, part type, and quantity
- CompletedLamps: contains information about each completed fog lamp, such as its ID, assembly station, and defect status
- Configurations: contains simulation configuration parameters, such as the time scale and defect rates
- PartBins: contains information about each part bin, such as its ID, part type, and current quantity
- TestTrays: contains information about each test tray, such as its ID and completion status

## Stored Procedures, Triggers, Views, and Functions
Stored procedures, triggers, views, and functions were created to support various activities in the database, such as updating part bin quantities, creating new completed lamps, and retrieving data for visualizations. Examples include:

- usp_UpdateBinQuantity: a stored procedure that updates the quantity of a part bin when a completed lamp is removed from it
- trg_CreateCompletedLamp: a trigger that creates a new completed lamp record when a lamp is completed at an assembly station
- vw_AssemblyStationStatus: a view that shows the current status of each assembly station, such as the number of lamps completed and defect rate

## C# Programs
Three C# programs were created to support the simulation:

- WorkstationSimulation: represents a single assembly station and provides the simulated timing surrounding the creation of a fog lamp
- WorkstationVisualization: displays a graphic representation of the part counts and status of a single assembly station in real time
- AssemblyLineVisualization: displays the status of the entire assembly line in real time, in the form of a conventional Kanban display

## Configuration
The Configurations table allows for full configuration of parameters for the simulation, such as the time scale and starting quantities of each part bin. Other parameters that can be configured include the defect rates for each skill level and the capacity of test trays

## Demo

