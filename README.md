# Companies Logo Free API

Welcome to the Companies Logo Free API! This project provides a simple and efficient way to fetch logos for publicly listed companies worldwide. By using the provided API, you can easily integrate company logos into your applications.

## Features

- **Free to Use**: No registration or API keys required.
- **Global Coverage**: Access logos for publicly listed companies from around the world.
- **Easy Integration**: Simple API endpoint to fetch logos in SVG format.
- **Comprehensive Data**: Utilizes a JSON file containing company slugs and exchange symbols.

## Getting Started

### Prerequisites

- Basic knowledge of HTTP requests.
- Access to the `companies.json` file containing company slugs and exchange symbols.

### Installation

No installation is required. You can start using the API directly by making HTTP requests to the provided endpoint.

### Usage

1. **Fetch Company Slugs**: Obtain the company slugs from the `companies.json` file. The file contains data in the following format:

    ```json
    {
        "totalCount": 131280,
        "data": [
            {
                "s": "SZSE:000001",
                "d": [
                    "ping-an"
                ]
            },
            {
                "s": "SZSE:000002",
                "d": [
                    "china-vanke-co"
                ]
            },
            ...
        ]
    }
    ```

2. **API Endpoint**: Use the following API endpoint to fetch the company logo:

    ```
    https://logo.tradient.org/v1/{slug}.svg
    ```

    Replace `{slug}` with the company slug obtained from the `companies.json` file.

### Example

To fetch the logo for "Ping An" with the slug `ping-an`, you would make a GET request to:

```
https://logo.tradient.org/v1/ping-an.svg
```

### Sample Code

Here is a sample code snippet in Python to fetch a company logo:

```python
import requests

# Company slug
slug = "ping-an"

# API endpoint
url = f"https://logo.tradient.org/v1/{slug}.svg"

# Make the GET request
response = requests.get(url)

# Check if the request was successful
if response.status_code == 200:
    # Save the logo to a file
    with open(f"{slug}.svg", "wb") as file:
        file.write(response.content)
    print(f"Logo for {slug} saved successfully.")
else:
    print(f"Failed to fetch logo for {slug}. Status code: {response.status_code}")
```

## Contributing

Contributions are welcome! If you have any suggestions, improvements, or bug fixes, feel free to create a pull request (PR). Here are some guidelines to follow:

1. Fork the repository and create a new branch for your feature or bug fix.
2. Make your changes and ensure they are well-documented.
3. Test your changes thoroughly.
4. Create a pull request with a clear description of your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

- Thanks to the contributors and maintainers of the `companies.json` file for providing comprehensive company data.
- Special thanks to the Tradient team for providing the logo API.

## Contact

For any questions or support, please open an issue in the GitHub repository.

---

Happy coding! We hope you find the Companies Logo Free API useful for your projects.