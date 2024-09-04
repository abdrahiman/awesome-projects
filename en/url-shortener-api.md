## ⭐ Goal

In this challenge, you will create a URL Shortener API. The goal is to build a service that takes long URLs as input, generates shorter, unique URLs, and redirects users to the original URL when they visit the shortened link. URL shorteners are commonly used to make sharing links easier and to track link clicks.

## 🚨 Requirements

1. **API Endpoints:**
    - **POST `/shorten`**: Accepts a long URL and returns a shortened version.
    - **GET `/r/{short_code}`**: Redirects users to the original long URL associated with the given short code.
2. **Database:** Use a simple database or in-memory store to map short codes to long URLs(sqlite3, txt filexs…).
3. **Short Code Generation:** Ensure that the short codes are unique, and consider implementing a method to generate them (e.g., base62 encoding or a hash function).
4. **Validation:** Validate that the input is a well-formed URL before shortening it.
5. **Redirection:** When a user visits the short URL, your API should perform a 301 or 302 redirect to the original URL.
6. **Error Handling:** Handle cases where the short code does not exist in the database, returning an appropriate error message.

## 💼 Usage
### Input

- ` POST /shorten`:
**Body:** A JSON object with a `url` field containing the long URL.
```json
{
    "url": "https://www.example.com/some/very/long/path"
}
```
    
- `GET /r/{short_code}`:
**Path Parameter:** The `{short_code}` representing the shortened URL.

### Output

- `POST /shorten`
    - **Response:** A JSON object with a `short_url` field containing the shortened URL:
    ```json
    {
    	"short_url": "http://yourdomain.com/r/abc123"
    }
    ```
    
- `GET /r/{short_code}`:
    - **Redirection:** A 301 or 302 redirect to the original long URL.

## 🧪 Testing

- Test the API by shortening various URLs and ensure that each short URL correctly redirects to the original.
- Verify that the short codes are unique and that no two different long URLs produce the same short code.
- Check the handling of invalid URLs and non-existent short codes to ensure that the API responds with appropriate error messages.

## 🍥 Bonus

- Implement a custom short code feature that allows users to specify their own short code instead of generating one.
- Add a feature to track and return the number of times each short URL has been accessed.
- Create a web interface where users can enter a long URL and receive the short URL, with an option to view analytics for their links.
- Support expiration dates for short URLs, after which they no longer redirect to the original URL.
