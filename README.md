# 🚀 CompaniesLogo - Free API

![GitHub repo size](https://img.shields.io/github/repo-size/yourusername/CompaniesLogo?color=blue&style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/yourusername/CompaniesLogo?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/yourusername/CompaniesLogo?style=for-the-badge)
![License](https://img.shields.io/github/license/yourusername/CompaniesLogo?style=for-the-badge)

Welcome to the **Companies Logo Free API**! This project provides a simple and efficient way to fetch logos for publicly listed companies worldwide. You can seamlessly integrate these logos into your applications.

---

## 🌟 Features

✅ **Free to Use** - No registration or API keys required.  
🌍 **Global Coverage** - Access logos for publicly listed companies from stock exchanges worldwide.  
⚡ **Easy Integration** - Simple API endpoint to fetch logos in **SVG format**.  
📂 **Comprehensive Data** - Utilizes a JSON file containing **company slugs and exchange symbols**.  

---

## 📌 Supported Stock Exchanges

| Exchange | Symbol |
|----------|--------|
| 🇺🇸 NYSE | `NYSE` |
| 🇺🇸 NASDAQ | `NASDAQ` |
| 🇬🇧 LSE | `LSE` |
| 🇩🇪 XETRA | `XETRA` |
| 🇨🇳 SZSE | `SZSE` |
| 🇯🇵 TSE | `TSE` |
| 🇮🇳 NSE | `NSE` |
| 🇦🇺 ASX | `ASX` |
| 🌎 More... | `Various` |

---

## 🚀 Getting Started

### Prerequisites

📌 Basic knowledge of **HTTP requests**.  
📌 Access to `companies.json` file containing company slugs and exchange symbols.  

### 🛠 Installation

No installation required! You can start using the API by making HTTP requests to the endpoint.

---

## 🔗 API Usage

### 1️⃣ Fetch Company Slugs

Get company slugs from the `companies.json` file. The file follows this format:

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
        }
    ]
}
```

### 2️⃣ API Endpoint

```url
https://logo.tradient.org/v1/{slug}.svg
```

Replace `{slug}` with the company slug from `companies.json`.

### 3️⃣ Example Request

To fetch the **Ping An** logo (`ping-an`):

```url
https://logo.tradient.org/v1/ping-an.svg
```

### 📜 Sample Code (Python)

```python
import requests

slug = "ping-an"
url = f"https://logo.tradient.org/v1/{slug}.svg"

response = requests.get(url)
if response.status_code == 200:
    with open(f"{slug}.svg", "wb") as file:
        file.write(response.content)
    print(f"Logo for {slug} saved successfully.")
else:
    print(f"Failed to fetch logo for {slug}. Status code: {response.status_code}")
```

---

## 🤝 Contributing

Contributions are **welcome**! If you have any improvements, bug fixes, or feature suggestions, follow these steps:

1️⃣ **Fork** the repository & create a new branch.  
2️⃣ **Make your changes** (document them well).  
3️⃣ **Test** your changes thoroughly.  
4️⃣ **Create a pull request** with a detailed explanation.  

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgments

🎉 Thanks to contributors and maintainers of the `companies.json` file for providing comprehensive data.  
🚀 Special thanks to **Tradient** for providing the logo API.  

---

## 📩 Contact

For support or questions, **open an issue** in the GitHub repository.

---

🚀 **Happy Coding!** We hope you find the Companies Logo Free API useful! 😊

