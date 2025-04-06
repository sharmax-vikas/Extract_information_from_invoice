
# Invoice Data Extraction using LayoutLMv2

This project demonstrates how to extract key information from invoices using the LayoutLMv2 model.  It leverages the `transformers` library and the `impira/layoutlm-document-qa` model to answer questions about invoice images.

## Project Structure

The project includes the following components:

1. **Installation:** Instructions for installing required libraries.
2. **Single Image Test:**  A test demonstrating how to extract information from a single invoice image.
3. **Dataset Processing:**  Code to load a dataset of invoices, display an example image, and ask questions about its contents.
4. **Image Saving:** Downloads a subset of the invoice dataset for local processing.
5. **Data Extraction and DataFrame Creation:**  Iterates through the downloaded images, extracts data using the LayoutLMv2 model, and compiles it into a Pandas DataFrame.


## Requirements

* Python 3.7+
* `transformers`
* `datasets`
* `pytesseract`
* `Pillow`
* `matplotlib`
* `pandas`
* `detectron2`


## Usage

1.  **Installation:**  Run the provided installation commands in a suitable environment.

2. **Running the Code:** Execute the Python script. It will:

    * Download a subset of the invoices dataset.
    * Process the downloaded images.
    * Extract information from each image based on the provided questions.
    * Create a pandas DataFrame which includes extracted information.

3. **Customization:**

    * Modify the `image_path` variable in the single image test section to point to your own invoice image.
    * Adjust the questions in the `questions` list to query the images for other information.
    * Modify the save directory to save images to a different location.

## Example Output

The script outputs a Pandas DataFrame containing the extracted information from each invoice image, including: image name, invoice number, tax ID, date, seller name, client name, gross worth, net worth and VAT values.



## Notes

* The accuracy of the extraction depends on the quality of the invoice images and the model's ability to interpret them.
* The `impira/layoutlm-document-qa` model is used, but other document question-answering models could be employed.
* Ensure that Tesseract OCR is correctly installed and configured on your system.

## Acknowledgments
* Impira for the LayoutLMv2 model (`impira/layoutlm-document-qa`).
* The Hugging Face team for the `transformers` library and the Datasets library.
