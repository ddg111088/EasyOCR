# BizCardX-Extracting_Business_Card_Data_with_OCR
## What is EasyOCR?
EasyOCR is an open-source, Python-based optical character recognition (OCR) library that can be used to extract text from images and documents. It is compatible with a wide range of languages and writing scripts, and it is known for its accuracy and speed. In my project I am using easyOCR to extract text from **business cards.**

EasyOCR is based on the Tesseract OCR engine, but it provides a number of additional features and improvements, such as:
-	Support for multiple languages and writing scripts
-	Faster recognition speed
-	Improved accuracy
-	Easier to use API
EasyOCR is a popular choice for a variety of OCR tasks, including:
-	Extracting text from scanned documents
-	Reading text from images of signs and labels
-	Identifying text in natural scene images
-	Translating text from one language to another

## Project Overview

BizCardX is a simple tool for extracting information from business cards. The programme recognises text on business cards with OCR technology and extracts the data into a SQL database after categorization with regular expressions. Users can view the retrieved data using a streamlit-built GUI. The BizCardX programme has a simple and straightforward user interface that takes users through the process of uploading the business card image and extracting its information. The extracted data would be displayed in a tidy and organised manner, and users would be able to effortlessly add it to the database with the click of a button. Furthermore, the data saved in the database may be quickly read, changed, and removed by the user as required.

### Want to see demo video of my project? - [click here]()

## Libraries/Modules used for the project!

   - Pandas - (To Create a DataFrame with the scraped data)
   - mysql.connector - (To store and retrieve the data)
   - Streamlit - (To Create Graphical user Interface)
   - EasyOCR - (To extract text from images)
   -PIL- (image module from the pillow and call the Image. open(), passing the image filename)
   - cv2 - OpenCV (OpenCV is the huge open-source library for the computer vision)
   - os - (OS module has methods for interacting with OS, such as creating files and directories)
   - matplotlib.pyplot -  (Pyplot is a collection of MATLAB-style functions for matplotlib)
  - re - (A regular expression (or RE) specifies a set of strings that matches it)


## Workflow

To get started with BizCardX Data Extraction, follow the steps below:
-	Install the required libraries using the pip install command. Streamlit, mysql.connector, pandas, easyocr.
-	pip install [Name of the library]
-	Execute the “BizCardX_main.py” using the streamlit run command.
streamlit run BizCardX_main.py

-	A webpage is shown in the browser, and I designed the app with three menu options: HOME, UPLOAD & EXTRACT, and MODIFY, where the user may upload the individual Business Card whose information must be extracted, saved, edited, or deleted if necessary.
-	Once user uploads a business card, the text present in the card is extracted by easyocr library.
-	Using loops and some regular expression, the extracted text is given to the get_data() function (user defined- I programmed this function) for text categorization as firm name, card holder name, designation, mobile number, email address, website URL, area, city, state, and pin code.
-	The categorised data is presented on the screen and can be updated by the user as needed.
-	When you click the Upload to Database button, the data is saved in the MySQL database. (Note: For connection establishment, provide the appropriate host, user, password, and database name in create_database, sql_table_creation, and connect_database.)
-	Furthermore, the uploaded data in the SQL Database may be accessed using the MODIFY menu for Read, Update, and Delete operations.


