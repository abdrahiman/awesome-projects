## ⭐ Goal

Create a web API that generates custom images based on a person's name. The API will take a name as input and produce a simple yet visually appealing image featuring the first letter of that name.

This functionality is commonly used in applications to create default profile pictures or avatars. Your task is to build a RESTful API endpoint that accepts a name, extracts its first letter, generates an image with that letter, and returns the image as the API response.

## 🚨 Requirements

1. Create a GET endpoint `/api/initial-image` that accepts a `name` parameter
2. Generate a 200x200 pixel PNG image with:
    - The first letter of the name (uppercase) in white
    - A random background color
3. Return the generated image as the API response

## 💼 Usage

### Input:

```bash
curl -X GET "<http://localhost:5000/api/avatar?name=John>" --output john_avatar.png
```

### Output

The above command will save a PNG image named `john_avatar.png` in your current directory. The image should be:

- 200x200 pixels in size
- Contain a white "J" (for John) centered on the image
- Have a randomly olored background

You can verify the output by opening the `john_avatar.png` file.

## 🧪 Testing

- Try the API with different names (e.g., "Alice", "Zhang", "Emma")
- Verify that each generated image correctly displays the first letter of the given name
- Check that the background color changes between requests
