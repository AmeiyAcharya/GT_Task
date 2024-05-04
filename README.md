# GT_Task
LLM Inference on form 10-Ks from SEC-EDGAR

Video Demo on Youtube:

# Steps:

- **Input**: Obtain the ticker symbol from a user-friendly Tkinter GUI.
- **Data Acquisition**: Utilize sec-edgar-downloader to gather all Form 10-K filings associated with the provided ticker.
- **Data Preparation**: Cleanse the extracted data, converting HTML to readable text format.
- **Section Extraction**: Employ Regex to isolate specific sections (e.g., Item 1A, 7, 7A) from the 10-K filings for each year.
- **Data Integration**: Combine section data across all available years.
- **Visualization**: Generate WordCloud visualizations, eliminating common stopwords for clarity.
- **Topic Modeling**: Implement Latent Dirichlet Allocation (LDA) on sections such as Item 1A and 7 for deeper insight.
- **Text Processing**: Prepare text for LLM inference, utilizing chunking.
- **Integration with Claude API**: Configure prompts tailored to each section, initializing the LLM with the relevant text.
- **Display Insight**s: Showcase insights derived from the LLM using a GUI.
- **Local Deployment**: Facilitate local deployment using the Mercury platform for demonstration.

# Tech Stack:

# Deriving Insights:

### References:


