Weather System – Java Project
A simple Java-based Weather Data Storage System that demonstrates how to manage temperature records for multiple cities and years using a 2D array.

 
 Features
 Delete records (reset to missing)
 Retrieve stored records
 Row-major traversal (year by year)
 Column-major traversal (city by city)
 Handle sparse data (only show available records)
 Complexity analysis (time & space)

 WeatherSystem.java
│
├── WeatherRecord         // Represents a single weather entry
├── WeatherDataStorage    // Stores and manages all records
└── main()                // Demonstrates the system




How It Works

1. Define cities and years
String[] cities = {"Delhi", "Mumbai", "Kolkata"};
int[] years = {2023, 2024, 2025};

2. Insert records
storage.insert(2023, "Delhi", 32.5);
storage.insert(2024, "Mumbai", 29.8);
storage.insert(2025, "Kolkata", 30.1);

3. Retrieve a record
System.out.println(storage.retrieve(2023, "Delhi")); // Output: 32.5

4. Delete a record
storage.delete(2024, "Mumbai");

🖥 Example Data Table
Year	Delhi	Mumbai	Kolkata
2023	32.5	-9999	-9999
2024	-9999	-9999	-9999
2025	-9999	-9999	30.1

🔹 -9999 means missing data



How to Run

Clone this repository:

git clone https://github.com/your-username/weather-system-java.git
cd weather-system-java


Compile the program:

javac WeatherSystem.java


Run the program:
java WeatherSystem

📊 Complexity
Operation	Time Complexity	Space Complexity
Insert / Delete	O(1)	O(N × M)
Retrieve	O(1)	O(N × M)
Row/Col Traversal	O(N × M)	O(N × M)
📜 License

This project is open-source and available under the MIT License.
