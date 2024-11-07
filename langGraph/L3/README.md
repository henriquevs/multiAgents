
# Lesson 3: Agentic Search

This lesson demonstrates an agentic approach to conducting searches, specifically integrating Tavily's API and DuckDuckGo for retrieving structured and unstructured data on various queries. The setup includes scraping, parsing, and presenting data in a readable format.

### Prerequisites

- Python 3.8+
- Required packages: `dotenv`, `tavily`, `requests`, `BeautifulSoup`, `duckduckgo_search`, `pygments`
- Load API key from `.env` file for Tavily connection.

### Experiment Overview

1. **Tavily Search Integration**:
   - Establishes a connection to Tavily's API to retrieve structured search results.
   - Example query demonstrates fetching specific details about Nvidia's new Blackwell GPU.

2. **Location-Specific Queries**:
   - Allows querying weather data for any city, showcasing how to tailor searches with user-specified parameters.
   - Implements a fallback mechanism for handling rate-limit exceptions from DuckDuckGo.

3. **Web Scraping for Dynamic Content**:
   - Uses DuckDuckGo to find relevant URLs and BeautifulSoup to extract content.
   - Demonstrates scraping and parsing weather information, converting HTML tags into structured text.

4. **Data Processing and Output Formatting**:
   - Cleans and compiles extracted data to a readable string format.
   - Parses JSON data and provides syntax-highlighted output for better readability.

### Usage Example

To run a search with Tavily API:
```python
result = client.search("What is in Nvidia's new Blackwell GPU?", include_answer=True)
print(result["answer"])
```

To perform a DuckDuckGo search and scrape content:
```python
query = "what is the current weather in San Francisco? Should I travel there today?"
url = search(query)[0]
soup = scrape_weather_info(url)
print(str(soup.body)[:50000])  # Limit output length for readability
```

### Additional Notes

- **Error Handling**: Implements a basic exception handling mechanism to manage search rate limits.
- **Image Inclusion**: Contains a sample output image, `google_sample.png`, showing a typical search result.
- **Data Cleaning**: Removes unnecessary whitespace to improve data presentation.

### License

This experiment is for educational purposes only.
