# Handwritten-Character-Recognition
Humans can understand the contents of an image simply by looking. We perceive the text on the image as text and can read it. Computers don't work the same way. They need something more concrete, organized in a way they can understand. This is where Handwritten Character Recognition kicks in.  
Handwritten Character Recognition involves the detection of text content on images and translation of the images to encoded text that the computer can easily understand. An image containing text is scanned and analyzed in order to identify the characters in it. Upon identification, the character is converted to machine-encoded text.

# What is OCR Handwritten Character Recognition?
Optical Character Recognition involves the detection of text content on images and translation of the images to encoded text that the computer can easily understand. An image containing text is scanned and analyzed in order to identify the characters in it. Upon identification, the character is converted to machine-encoded text.
How is it really achieved? To us, text on an image is easily discernible and we are able to detect characters and read the text, but to a computer, it is all a series of dots.

The image is first scanned and the text and graphics elements are converted into a bitmap, which is essentially a matrix of black and white dots. The image is then pre-processed where the brightness and contrast are adjusted to enhance the accuracy of the process.

The image is now split into zones identifying the areas of interest such as where the images or text are and this helps kickoff the extraction process. The areas containing text can now be broken down further into lines and words and characters and now the software is able to match the characters through comparison and various detection algorithms. The final result is the text in the image that we're given.

The process may not be 100% accurate and might need human intervention to correct some elements that were not scanned correctly. Error correction can also be achieved using a dictionary or even Natural Language Processing (NLP).

The output can now be converted to other mediums such as word documents, PDFs, or even audio content through text-to-speech technologies.

# Uses of OCR

Previously, digitization of documents was achieved by manually typing the text on the computer. Through OCR, this process is made easier as the document can be scanned, processed and the text extracted and stored in an editable form such as a word document.

If you have a document scanner on your phone, such as Adobe Scan, you have probably encountered OCR technology in use.

Airports can also use OCR to automate the process of passport recognition and extraction of information from them.

Other uses of OCR include automation of data entry processes, detection, and recognition of car number plates.


# What we'll Use

For this OCR project, we will use the Python-Tesseract, or simply PyTesseract, library which is a wrapper for Google's Tesseract-OCR Engine.

I chose this because it is completely open-source and being developed and maintained by the giant that is Google. Follow these instructions to install Tesseract on your machine, since PyTesseract depends on it.

We will also use the Flask web framework to create our simple OCR server where we can take pictures via the webcam or upload photos for character recognition purposes.

We are also going to use Pipenv since it also handles the virtual-environment setup and requirements management.

Besides those, we'll also use the Pillow library which is a fork of the Python Imaging Library (PIL) to handle the opening and manipulation of images in many formats in Python.

In this post, we'll concentrate on PyTesseract although there are other Python libraries that can help you extract text from images such as:

    -Textract: which can extract data from PDFs but is a heavy package.
    -Pyocr   : offers more detection options such as sentences, digits, or words.


# Setup

1. Start by installing Pipenv using the following command via Pip (In case you need to set it up, refer to this).
   - $ pip install pipenv

2. Create the project directory and initiate the project by running the following command:
   - $ mkdir ocr_server && cd ocr_server && pipenv install --three

3. We can now activate our virtual environment and start installing our dependencies:
   - $ pipenv shell
   - $ pipenv install pytesseract Pillow 

In case you'll not be using Pipenv, you can always use the Pip and Virtual Environment approach. Follow the official documentation to help you get started with Pip and Virtual Environment. 
Note: In that case, instead of pipenv install Pillow, the command will be pip install Pillow.

