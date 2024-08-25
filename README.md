
### Adding a Copy Button

For a Markdown file (`README.md`), there isn’t a built-in way to add a "Copy" button. However, you can add HTML and JavaScript if your Markdown renderer supports it (e.g., GitHub Pages, some documentation generators). Here’s an example of how you might include a copy button with HTML and JavaScript:

```markdown
## API Endpoint

### `GET /api/airport`

#### Description

Retrieves detailed information about an airport based on its IATA code. Returns information about the airport, the city it is located in, and the country of that city.

#### Request Parameters

- `iata_code` (required): The IATA code of the airport.

#### Example Request

- **API URL:** 
  <input type="text" value="https://your-api-url.com/api/airport" id="apiUrl" readonly style="width: 100%; padding: 5px; margin-bottom: 10px;" />
  <button onclick="copyToClipboard()">Copy URL</button>

  <script>
    function copyToClipboard() {
      var copyText = document.getElementById("apiUrl");
      copyText.select();
      document.execCommand("copy");
      alert("API URL copied to clipboard: " + copyText.value);
    }
  </script>

- **Example Call:**

  ```bash
  curl "https://your-api-url.com/api/airport?iata_code=AGR"
