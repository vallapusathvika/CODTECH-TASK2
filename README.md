# CODTECH-TASK2
COMPANY:CODTECH IT SOLUTIONS

NAME:VALLAPU SATHVIKA

INTERN ID:CT08RGJ

DOMAIN:PYTHON PROGRAMMING

DURATION:4 WEEKS

MENTOR:NEELA SANTOSH

DESCRIPTION OF THE CODE* This Python code is designed to load, analyze, and visualize a dataset related to labour, capital, output, and wages, and then generate a comprehensive PDF report summarizing the findings. It is implemented using a Jupyter Notebook, which allows for interactive data analysis and visualization. The code utilizes several Python libraries, including Pandas, Matplotlib, FPDF, and Seaborn, to handle data, create visualizations, and generate the report.

Step 1: Loading Data The first step in the code is to load the dataset from a CSV file. The function load_data() uses the Pandas library to read the CSV file with the pd.read_csv() function. The path to the file is specified in the file_path variable. After loading the data, the column names are stripped of any leading or trailing spaces using df.columns.str.strip() to ensure that the column names are clean and consistent. This is important for data preprocessing and prevents errors in later steps. The function then prints out the names of the columns in the dataset to confirm their accuracy and returns the DataFrame containing the data. This operation is performed in the Jupyter Notebook, allowing users to visually inspect the dataset’s structure.

Step 2: Data Analysis The second part of the code involves analyzing the data to derive insights. The analyze_data() function performs this task. It first checks if the dataset contains the necessary columns: capital, labour, output, and wage. If any of these columns are missing, the function raises a KeyError with a message indicating which columns are missing. Once the required columns are confirmed, the function computes several important metrics:

Summary statistics: The df.describe() function is used to calculate basic statistics like mean, standard deviation, minimum, maximum, and percentiles for the capital, labour, output, and wage columns.
Correlation matrix: The function computes the correlation matrix using df.corr(), which shows the relationships between the different variables (capital, labour, output, and wage).
Total values: The function calculates the total capital, total labour, and total output using .sum(), and the average wage is calculated using .mean().
These results provide valuable insights into the dataset and can be examined further in the Jupyter Notebook, where the user can interactively view and manipulate the data.

Step 3: Plotting Capital vs Output The third step involves generating a plot to visualize the relationship between capital and output. The plot_capital_output() function creates a line plot using Matplotlib, which is a powerful visualization library in Python. The plot displays capital on the x-axis and output on the y-axis. Markers are added to the plot to indicate each data point. The plot is customized with a title, axis labels, and a grid for better readability. After generating the plot, it is saved as a PNG file using plt.savefig(), and the plot is closed with plt.close(). The path of the saved plot is returned for later use in the report. This plot can be displayed directly within the Jupyter Notebook, allowing users to visually assess the data.

Step 4: Generating the PDF Report The fourth step is to generate a PDF report summarizing the analysis. The generate_pdf_report() function uses the FPDF library, which allows the creation of PDF documents. The function adds a title to the report and includes sections for the summary statistics, the correlation matrix, and the total values for capital, labour, output, and the average wage. Additionally, it embeds the previously created plot in the report. The PDF is then saved to the specified location on the disk. This PDF report serves as a professional summary of the analysis, and users can easily share or print it. This functionality is integrated into the Jupyter Notebook for seamless workflow.

Step 5: Bringing It All Together The main() function is responsible for executing the entire process. It calls the load_data(), analyze_data(), plot_capital_output(), and generate_pdf_report() functions in sequence. If any required columns are missing, an error is caught, and a message is displayed, preventing further execution. This modular approach allows users to interactively run different parts of the analysis in the Jupyter Notebook, making it easy to adjust and refine the workflow as needed.

Conclusion In summary, this code is implemented in a Jupyter Notebook, allowing users to interactively load, analyze, and visualize economic data. The use of Pandas for data manipulation, Matplotlib for plotting, and FPDF for PDF report generation makes the code a powerful tool for automated data analysis. The ability to display plots directly within the notebook and generate a professional PDF report at the end enhances the overall workflow, making it suitable for both analysis and presentation purposes. This approach provides a seamless way to analyze and communicate insights from the data while leveraging the interactive capabilities of a Jupyter Notebook.

