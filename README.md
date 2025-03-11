# AI + ArcGIS Speedgeeking Demos

This repository contains two simple web applications showcasing how to integrate generative AI (via Google’s Gemini API) with the ArcGIS Maps SDK for JavaScript to dynamically highlight geospatial features. You can:

- Highlight **Countries** on a world map.
- Highlight **US States** on a map.

> **Note**: Both apps use the same `config.js` file (containing the API keys), which you must update with valid credentials.

## Key Files

1. **`CountriesLayer.html`**  
   - Demonstrates highlighting countries.

2. **`StatesLayer.html`**  
   - Demonstrates highlighting US states.

3. **`config.js`**  
   - Exports your `googleGeminiApiKey` and `arcgisApiKey`.  
   - **Important**: Replace `"your_gemini_key"` and `"your_arcgis_key"` with valid credentials.

## Setup & Configuration

1. **Clone or Download** this repository.

2.  **Obtain API keys**: Visit [Google AI Studio](https://aistudio.google.com/) and [ArcGIS Location Platform](location.arcgis.com) to obtain your own Google Gemini and ArcGIS API keys.

3. **Edit `config.js`** and set:
   ```js
   export const config = {
     googleGeminiApiKey: "YOUR_GOOGLE_GEMINI_API_KEY",
     arcgisApiKey: "YOUR_ARCGIS_API_KEY",
   };


---
## Usage

### 1. Open the Application

- **Countries Layer Demo:** Open `CountriesLayer.html` in your browser.  
- **States Layer Demo:** Open `StatesLayer.html` in your browser.

### 2. Enter a Query

1. In the **right column**, locate the text input field.  
2. Enter a query. For example:  
   - `List the top 5 most populous countries.`
   - `List the top 3 hottest states.`

### 3. Click "Submit"

- The application sends your query to Google’s Gemini API.
- Gemini returns a response in a specific format:
  - A numbered list of countries/states.
  - An “Explanation” line describing why those areas were chosen.

### 4. See Results

1. **Highlighted Features on the Map**  
   - Each country or state identified by the AI is highlighted in red on the map.
2. **List of Features**  
   - The **right column** displays the list of returned place names in a numbered list.
3. **Explanation**  
   - Below the list, you’ll see a one-sentence “Explanation” generated by the AI.

### 5. Try Different Queries

Feel free to experiment with various prompts:
- `List the top 5 countries by GDP.`
- `List the biggest oil-producing states.`
- `List the top 3 countries with the largest forest area.`

The AI will parse your request, return relevant geographic names, and highlight them on the map.

### 6. Troubleshooting

- If the map does not update or you see an error, ensure you have valid **Google Gemini** and **ArcGIS** API keys, and check your **browser console** for any relevant error messages.

## Gemini API Pricing (Gemini 1.5 Flash)
This application uses the gemini-1.5-flash model. Here's a quick overview of its pricing:
- **Input Price:** $0.075 per 1 million tokens (prompts <= 128k tokens), $0.15 (prompts > 128k tokens)
- **Output Price:** $0.30 per 1 million tokens (prompts <= 128k tokens), $0.60 (prompts > 128k tokens)
- **Context caching price:** $0.01875, prompts <= 128k tokens, $0.0375, prompts > 128k tokens.
- **Context caching storage:** $1.00 per hour.

### Token Usage and Pricing Explained

Gemini API costs are based on "tokens," which are pieces of words.

* **Input Tokens:** Your question's length.
* **Output Tokens:** Gemini's answer length.

Longer questions and answers = more tokens = higher cost.

Keep queries short to save costs. Google offers a free tier for testing. See the [Gemini API pricing page](https://ai.google.dev/gemini-api/docs/pricing) for details.

## License

These demos are provided under the [MIT License](LICENSE) (or whichever license you choose to include). Feel free to modify and adapt them for your own presentations, demos, or projects.

## YouTube Video Tutorial

Check out my [video version](https://www.youtube.com/watch?v=MbfRpU8-Ya0) of this app using Esri Leaflet!

**Enjoy exploring AI-driven geospatial visualizations!**
