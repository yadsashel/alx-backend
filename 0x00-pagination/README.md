# Pagination Project

This project implements pagination techniques for a dataset of popular baby names, using a CSV file as the data source. The code provides various pagination methods that make it easier to display large datasets page-by-page.

## Project Overview

The project is structured around the `Server` class, which:
1. Reads data from a CSV file (`Popular_Baby_Names.csv`).
2. Supports multiple pagination methods:
   - **Basic Pagination**: Splits data into pages based on `page` and `page_size`.
   - **Hypermedia Pagination**: Returns pages with additional information, such as whether a "next" or "previous" page exists.
   - **Deletion-Resilient Pagination**: Ensures pagination remains accurate if items are removed from the dataset.

## Files

- **`Popular_Baby_Names.csv`**: The CSV file containing the dataset.
- **`server.py`**: Contains the `Server` class and functions for pagination.
- **`README.md`**: This file, providing an overview of the project.

## Requirements

- Python 3.x
- `Popular_Baby_Names.csv` in the same directory as `server.py`

## Getting Started

1. Clone the repository.
2. Ensure the `Popular_Baby_Names.csv` file is in the same directory as your script.
3. Run the script using Python.

## Functions Overview

### `index_range(page: int, page_size: int) -> Tuple[int, int]`
Calculates the start and end indexes for a given page.

### `Server` Class

- **`dataset(self) -> List[List]`**: Loads data from the CSV file.
- **`get_page(self, page: int, page_size: int) -> List[List]`**: Returns a specific page of data.
- **`get_hyper(self, page: int, page_size: int) -> Dict`**: Returns a page of data along with additional pagination info (next/previous page, total pages).
- **`get_hyper_index(self, index: int = None, page_size: int = 10) -> Dict`**: Ensures pagination remains accurate if data is deleted from the dataset.

## Usage Examples

```python
server = Server()

# Get page 1 with 5 items per page
page_data = server.get_page(1, 5)

# Get hypermedia pagination for page 2 with 10 items per page
hyper_data = server.get_hyper(2, 10)

# Get deletion-resilient pagination data for a page with index 5 and size 3
resilient_data = server.get_hyper_index(5, 3)
```

## Additional Information

### Pagination Types

1. **Basic Pagination**: Splits the dataset into numbered pages.
2. **Hypermedia Pagination**: Adds details like current page, total pages, next/previous page indicators.
3. **Deletion-Resilient Pagination**: Adjusts page contents if dataset changes, ensuring data is displayed without gaps or repeats.
