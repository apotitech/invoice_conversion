# Invoice Conversion Package

## Description

The `invoice_conversion` package provides a seamless way to convert Excel invoice files into a PDF format. Whether you have a business or personal invoices that need converting, this tool streamlines the process, presenting you with a professional-looking PDF invoice.

## Table of Contents

- [Invoice Conversion Package](#invoice-conversion-package)
  - [Description](#description)
  - [Table of Contents](#table-of-contents)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Contributing](#contributing)
  - [Future Enhancements](#future-enhancements)
  - [Issues](#issues)
  - [License](#license)

## Installation

To install the package, use `pip`:

```bash
pip install invoice_conversion
```

Please before you proceed, make sure you have the following dependencies installed:

- pandas
- fpdf

They can be installed using `pip`:

```bash
pip install pandas fpdf
```

## Usage

Here's a basic usage guide:

1. Import the package:
   
   ```python
   from invoice_conversion import InvoicePDF
   ```

2. Instantiate the `InvoicePDF` class:

   ```python
    invoice_pdf_generator = InvoicePDF(
    invoices_path="path/to/excel/invoices",
    pdfs_path="path/to/output/pdf",
    company_name="Your Company Name",
    logo_path="path/to/company/logo.png"
    )
   ```

3. Next use the `generate_all` method to generate PDFs:
   
   ```python
   invoice_pdf_generator.generate_all(
    product_id="product_id_column_name",
    product_name="product_name_column_name",
    amount_purchased="amount_purchased_column_name",
    price_per_unit="price_per_unit_column_name",
    total_price="total_price_column_name"
    )
   ```

Make sure to **replace the placeholders** in the function call with **appropriate paths** and **column names** from your **Excel invoices**.

## Contributing

We welcome contributions! If you'd like to contribute, please go ahead and fork the repository, make your suggested changes, and open a pull request.

## Future Enhancements

- Support for multiple currencies.
- OCR (Optical Character Recognition) integration to automatically detect columns in the Excel sheets.
- Customizable PDF templates to allow users more control over the appearance of the output PDF.
- A user-friendly GUI application for less tech-savvy users.

## Issues

If you encounter any issues while using the package or have any feature requests, please visit the [issues page](https://github.com/apotitech/invoice_conversion/issues) of our GitHub repository. We appreciate your feedback and will strive to address any concerns promptly.

## License

This project is licensed under the MIT License. For more details, please see the LICENSE file in the repository.
