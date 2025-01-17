# TSP-Hill-Climbing
"Streamlit app for solving the Traveling Salesperson Problem using the Hill Climbing algorithm with MySQL integration."
Features
Random Solution Generator: Generates a random route for the TSP based on the provided distance matrix.
Hill Climbing Optimization: Iteratively improves the solution by evaluating all neighboring routes and selecting the best one.
Database Integration: Saves the best solution and its route length into a MySQL database for later reference.
Interactive UI: User-friendly interface built with Streamlit for running the algorithm and visualizing results.
Requirements
Python 3.7 or higher
MySQL Server installed and running
Required Python libraries:
streamlit
mysql-connector-python
Installation
Clone the repository:

bash
Copy
Edit
git clone https://github.com/username/TSP-Hill-Climbing.git
cd TSP-Hill-Climbing
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Set up MySQL:

Create a database named hillclimbing in MySQL.
Update the database credentials in the save_to_mysql function inside the code:
python
Copy
Edit
connection = mysql.connector.connect(
    host='localhost',
    user='your_mysql_username',
    password='your_mysql_password',
    database='hillclimbing'
)
Usage
Run the Streamlit app:

bash
Copy
Edit
streamlit run app.py
Open your browser and go to http://localhost:8501.

Steps to use the app:

Enter Distance Matrix: Input the distance matrix (e.g., [[0, 1, 2], [1, 0, 3], [2, 3, 0]]).
Generate Random Solution: Click the button to create an initial random route.
Run Hill Climbing: Optimize the random route using the Hill Climbing algorithm.
Export to MySQL: Save the best solution and its route length to the database.
Example
Input distance matrix:

python
Copy
Edit
[[0, 1, 2],
 [1, 0, 3],
 [2, 3, 0]]
Output:
Random Solution: [2, 0, 1]
Random Solution Length: 6
Optimized Solution: [0, 2, 1]
Optimized Route Length: 4
File Structure
app.py: Main application script.
requirements.txt: List of dependencies.
.gitignore: Specifies files and directories to ignore in the repository.
Future Enhancements
Add visualization of the TSP route.
Support larger datasets with performance optimizations.
Include other optimization algorithms (e.g., Simulated Annealing, Genetic Algorithms).
Improve error handling for invalid inputs.
