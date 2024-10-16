### Web Scraping Project - Pharma Conference Data Extraction

This project was designed to automate the extraction of session and presentation data from the **UEG Programme** and **UEG Industry Sessions** websites. Several key decisions were made in the development process to ensure efficient data retrieval, organization, and keyword matching. 


### Design and Implementation Choices

- **Choice of Tools and Libraries**: 
  - **Python** was chosen as the primary language due to its versatility and extensive libraries for data manipulation and web scraping.
  - The **Requests** library was selected for making HTTP requests, as it provides a simple yet powerful way to interact with the websites’ APIs and retrieve session and presentation data.
  - **Pandas** was used to organize the scraped data into structured formats and export it to Excel, as it provides an efficient framework for data manipulation.
  - **Poetry** was chosen for dependency management and project packaging. Its use of a `pyproject.toml` file simplifies tracking and managing libraries, ensuring that the project runs with the correct versions of dependencies.
  - **Jupyter Notebooks** were utilized for prototyping and iterative testing of the scraping logic. This environment allows for interactive data exploration, making it easier to visualize and manipulate data during development.
  - **JSON** was employed as the primary data format for handling API responses. Its lightweight structure facilitates easy parsing and manipulation, allowing for efficient extraction of necessary information from the web.

 #### Future implementations posssibility:
 
1. Real-Time Data Updates
   
- Current Limitation: The project scrapes data on demand, but it does not handle updates or changes to conference sessions in real time.
- Future Implementation: Integrating a real-time data monitoring system using webhooks or periodic background tasks could keep the dataset up to date. This would allow the tool to automatically capture changes in session details or new presentations added after the initial scrape.

3. Cloud-Based Deployment
- Current Limitation: The project runs locally and relies on manual execution.
- Future Implementation: Deploying the scraper to a cloud platform (e.g., AWS, Azure) and scheduling it as a serverless function would automate the scraping process entirely. This would also allow for scalability, handling larger datasets without performance bottlenecks on local machines.

5. Asynchronous Requests
   
- Current Limitation: The project currently makes HTTP requests sequentially, which can slow down the scraping process, especially when handling multiple pages or sessions.
- Future Implementation: Utilizing asynchronous programming with libraries like aiohttp or httpx could significantly reduce the time spent waiting for responses from the server. This approach would allow multiple requests to be processed concurrently, leading to faster data retrieval.

7. Batch Processing
   
- Current Limitation: Each request is handled individually, which can lead to inefficiencies in the data extraction workflow.
- Future Implementation: Implementing batch processing could allow the tool to request and process multiple pages or sessions in one go, rather than one at a time. This could be particularly beneficial when dealing with paginated APIs.
