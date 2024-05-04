# GT_Task
LLM Inference on form 10-Ks of an Instrument from SEC-EDGAR

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

# Deriving Insights:

1. `List the key trends or changes in the company's business operations and financial performance over the past few years based on the information provided in Item 1A (Risk Factors)?`
    - The Risk Factors section discloses the most significant risks that could adversely impact the company's business, operations, industry or financial results. Analyzing trends in these risks over time provides insight into how the company's risk profile is evolving.
    - Evaluating how these various types of risks are changing gives a comprehensive view of the company's overall risk exposure.
    - Research has shown that changes in risk factor disclosures are associated with future changes in firm performance and stock returns [The_Benefits_of_Specific_Risk-Factor_Disclosures](https://www.researchgate.net/publication/272245080_The_Benefits_of_Specific_Risk-Factor_Disclosures)

2. `Based on the (MD&A) section in Item 7, what are the main factors driving the company's revenue growth or decline, and how does the company plan to address these factors going forward?`
    - The MD&A provides management's perspective on the company's financial condition, changes in financial condition, and results of operations. It explains the drivers behind revenue and profitability trends.
    - Management discusses the key factors and trends impacting revenues, such as volume, pricing, new products, competition, etc. This disaggregation is essential to understand what's really driving the top line.
    - [The_Usefulness_of_MDA_Disclosures_in_the_Retail_Industry](https://www.researchgate.net/publication/254109721_The_Usefulness_of_MDA_Disclosures_in_the_Retail_Industry)

3. `According to Disclosures about Market Risk in Item 7A, what are the most significant market risks the company faces, and how does it manage or mitigate these risks?`
    - This section requires companies to disclose information about market risk exposures from financial instruments, like interest rate risk, foreign currency risk, commodity price risk, and equity price risk.
    - The quantitative disclosures estimate the potential loss in future earnings, fair values, or cash flows from market risk sensitive instruments.

To Be Explored:

`Item 1B. Unresolved Staff Comments`
"Impact of Employee Morale on Organizational Success" (https://www.ijrte.org/wp-content/uploads/papers/v8i4/D8070118419.pdf): This research suggests a strong link between high employee morale and positive financial outcomes. Unresolved staff concerns highlighted in the 10K could indicate potential morale issues that might impact future performance.

# Tech Stack:
`Jupyter Notebook` is a popular platform for data analysis and visualization, making it suitable for this task. It allows for easy and interactive exploration of the data.

`Mercury` is used for deployment, allowing for easy deployment of the model and its associated functionalities locally.

The libraries used in this tech stack, such as `requests`, `lxml`, `bs4`, `pandas`, `numpy`, `sklearn`, `matplotlib`, `nltk`, `gensim`, `wordcloud`, `pyLDAvis`, `seaborn`, `textblob`, `pandas_datareader`, `anthropic`, `sec_edgar_downloader`, `tkinter` and `BeautifulSoup`, provide the necessary functionalities for tasks such as automation, downloading, cleaning, extracting, processing, getting insights, doing LLM api inference, visualization, and web scraping.

Overall, this tech stack ensures a seamless and efficient workflow for performing LLM inference on EDGAR form 10-K annual reports, enabling effective analysis and interpretation of the data.
