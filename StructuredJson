import json
import pandas as pd
import os

def sorter(json_file_path, output_file):
    
    try:

        if not os.path.exists(json_file_path):
            print(f"Error: File '{json_file_path}' not found.")
            return
        
        with open(json_file_path, 'r', encoding='utf-8') as file:
            json_data = json.load(file)

        if not isinstance(json_data, list):
            print("Error: The JSON file must contain a list of dictionaries.")
            return

        df = pd.DataFrame(json_data)

        df.to_excel(output_file, index=False, engine='openpyxl')

        print(f"Data has been successfully written to {output_file}")

    except json.JSONDecodeError:
        print("Error: Failed to decode JSON. Ensure the file contains valid JSON.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")

json_file_path = r"C:\Users\Kaustubh\Documents\Projects\Python\input.json"
output_file = r"C:\Users\Kaustubh\Documents\Projects\Python\output.xlsx"


sorter(json_file_path, output_file)
