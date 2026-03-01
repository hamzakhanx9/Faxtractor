# Faxtractor Chrome Extension

Faxtractor is a simple Chrome extension designed to extract article text from web pages by gathering paragraph (`<p>`) elements. The extension can be triggered from a popup and sends the extracted content to either display or process further.

## Features

- Collects all paragraph text from the current page.
- Communicates between content script and popup via `chrome.runtime` messaging.
- Easy to extend for additional content extraction or analysis.

## Project Structure

```
content.js      - Content script that extracts paragraph text and listens for messages.
popup.html      - Popup interface for the extension.
popup.js        - Logic to request article text from the content script.
manifest.json   - Chrome manifest defining permissions and script entries.
``` 

## Installation

1. Clone or download the repository.
2. Open Chrome and navigate to `chrome://extensions`.
3. Enable "Developer mode".
4. Click "Load unpacked" and select the project directory.

## Usage

1. Navigate to any article page in Chrome.
2. Click the Faxtractor extension icon.
3. The popup will request the page's paragraph text from the content script and display or handle it accordingly.

> **Note:** Before using the popup you may need to configure a GitHub access token. Add your token to `popup.js` (e.g. set a `GITHUB_TOKEN` constant) if the extension submits data to GitHub or uses the API.

## Development

- Modify `content.js` to change extraction logic.
- Update `popup.js` for UI or messaging changes.
- Adjust permissions in `manifest.json` if adding new features.

## Contributing

Feel free to open issues or submit pull requests for enhancements or bug fixes.

## License

This project is open source and available under the [MIT License](LICENSE) (add LICENSE file if desired).
