# CAPTCHA Solver Application

This is a simple single-file web application designed to demonstrate a basic client-side CAPTCHA challenge and solution mechanism. It uses Tailwind CSS for a modern, responsive user interface.

## Features

-   **Responsive Design:** Optimized for various screen sizes using Tailwind CSS.
-   **CAPTCHA Display:** Shows an image-based CAPTCHA.
-   **URL Parameter Support:** Can load CAPTCHA images from an external URL provided via a query parameter (`?url=https://.../image.png`).
-   **Default Image:** Defaults to a local `sample.png` if no URL is specified.
-   **Client-Side Validation:** For the `sample.png` image, it validates the user's input against the expected CAPTCHA text ("ADUR3").
-   **Simulated Submission:** For external CAPTCHA images, it simulates a submission, as real-time solving of arbitrary CAPTCHAs requires advanced server-side image processing or machine learning.

## How to Use

### 1. Locally with Default Image

1.  Save `index.html`, `README.md`, `LICENSE`, and `sample.png` in the same directory.
2.  Open `index.html` in your web browser.
3.  You will see the `sample.png` CAPTCHA image (which reads "ADUR3").
4.  Type "ADUR3" (case-insensitive) into the input field and click "Solve CAPTCHA". The application will report "Correct!".

### 2. With an External CAPTCHA Image URL

1.  Open `index.html` in your web browser, appending a `?url=` query parameter with the desired image URL.
    Example: `index.html?url=https://example.com/some-captcha-image.png`
2.  The application will display the image from the provided URL.
3.  Type what you see in the CAPTCHA image into the input field and click "Solve CAPTCHA".
4.  The application will report that your input was submitted (e.g., "Submitted: 'your_text'."). Note that for external images, actual validation against the CAPTCHA content is not performed client-side.

## Limitations

-   This is a client-side demonstration. A true CAPTCHA solver for arbitrary images typically involves complex server-side image recognition (e.g., OCR, machine learning models).
-   The "solver" for external URLs merely accepts user input and acknowledges submission; it does not actually *solve* the CAPTCHA content from the provided URL.

## Technologies Used

-   HTML5
-   Tailwind CSS (via CDN)
-   Vanilla JavaScript

## License

This project is open-source and available under the MIT License. See the `LICENSE` file for more details.