# SDS Data Extractor

A web application for extracting chemical data from Safety Data Sheet (SDS) PDFs and merging it with existing Excel files.

## Features

- Upload a ZIP file containing multiple SDS PDFs
- Select an existing Excel file to update
- Extract chemical data like CAS Numbers, Flash Points, Density, etc.
- Merge entries by CAS Number to avoid duplicates
- Download the updated Excel file

## Installation

1. Clone the repository
2. Install frontend dependencies:
   ```
   npm install
   ```
3. Install Python backend dependencies:
   ```
   pip install -r requirements.txt
   ```

## Running the Application

1. Start the backend server:
   ```
   python app.py
   ```
2. In a separate terminal, start the frontend development server:
   ```
   npm run dev
   ```
3. Open your browser and navigate to the URL shown in the terminal (usually http://localhost:5173)

## How It Works

1. Upload a ZIP file containing multiple SDS PDFs and select your existing Excel file.
2. The backend extracts the ZIP file and processes each PDF with pdfplumber.
3. Chemical data is extracted using pattern matching.
4. Data is merged with the existing Excel file, avoiding duplicates based on CAS Number.
5. The updated Excel file is provided for download.

## Technologies Used

- Frontend: React, TypeScript, Tailwind CSS, Vite
- Backend: Flask, Python
- Data Processing: pdfplumber, pandas, openpyxl