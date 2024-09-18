### ⭐ Goal

In this challenge, you will develop a web crawler, a program designed to traverse the internet by following links on web pages. The crawler's job is to index the content of websites, gathering information such as URLs, page titles, and meta descriptions. This data is often used by search engines to provide relevant search results or by data analysts for various insights.

Your task is to build a web crawler that starts at a given URL, explores the website, and indexes the content of all the pages it encounters.

### 🚨 Requirements

- **Start URL**: The crawler should start crawling from a provided URL.
- **Depth Limitation**: The crawler should limit its search to a specified depth, where depth `1` means only the starting page, depth `2` means the starting page and pages linked from it, and so on.
- **Content Extraction**: For each page visited, extract and store the following:
    - Page URL
    - Page title (found in the `<title>` tag)
    - Meta description (found in the `<meta name="description" content="...">` tag)
- **Handling Errors**: The crawler should handle and report errors, such as 404 (Not Found) and 500 (Internal Server Error) responses.
- **Respect `robots.txt`**: The crawler should respect the `robots.txt` file of each website, which indicates which parts of the site should not be crawled.
- **Output Format**: The crawler should output the results in a structured format such as JSON or CSV.

### 💼 Usage

### Input

- **start_url**: A string representing the URL where the crawler should start.
- **depth**: An integer representing how deep the crawler should traverse the website.

### Output

- A structured list of indexed pages, where each page includes:
    - URL
    - Title
    - Meta description

Example:

```json
[
  {
    "url": "https://example.com",
    "title": "Example Domain",
    "meta_description": "This domain is for use in illustrative examples in documents."
  },
  {
    "url": "https://example.com/about",
    "title": "About Example Domain",
    "meta_description": "Learn more about Example Domain."
  }
]
```

### 🧪 Testing

- **Test Case 1**: Start URL `https://example.com`, depth `1`. The crawler should only return data from the main page.
- **Test Case 2**: Start URL `https://example.com`, depth `2`. The crawler should return data from the main page and any pages linked from it.
- **Test Case 3**: A URL with an unreachable page (e.g., a 404 error). The crawler should handle this gracefully and continue.
- **Test Case 4**: A website with a `robots.txt` file that restricts certain pages. The crawler should obey these restrictions.
- **Test Case 5**: Verify that it does not follow links to external domains.

### 🍥 Bonus

- Extend the crawler to handle websites with dynamically loaded content (e.g., pages that require JavaScript to render content).
- Implement a multi-threaded version of the crawler to increase its efficiency.
- Create a user interface where users can input a URL and view the indexed content directly on the website.
- Add a feature that visualizes the structure of the crawled website, showing connections between pages.
