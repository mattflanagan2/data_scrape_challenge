# Challenge
This new assignment consists of two technical products. You will submit the following deliverables:

Deliverable 1: Scrape titles and preview text from Mars news articles.

Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

##  Part 1: Scrape Titles and Preview Text from Mars News
### Step 1
First, I used automated browsing to visit the Mars news site. I inspected the page to identify which elements to scrape.

<img width="1295" alt="Screenshot 2024-04-01 at 11 52 59 AM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/8498c621-cffd-4c89-b0f8-e9df46614337">

### Step 2
Next, I extracted the titles and preview text of the news articles that I scraped and stored the scraping results in Python data structures.

<img width="1295" alt="Screenshot 2024-04-01 at 11 59 50 AM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/ab8a8ae5-c6f6-4e30-ac27-ed316038e954">

### Step 3
Next, I stored each title-and-preview pair in a Python dictionary and gave each dictionary two keys: title and preview and stored all the dictionaries in a Python list.
then printed the list in my notebook.

<img width="1295" alt="Screenshot 2024-04-01 at 12 02 40 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/5c9359c0-bbcd-466c-a2e2-d7c4f6acc823">
<img width="1295" alt="Screenshot 2024-04-01 at 12 02 54 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/73c4d61a-faad-437f-8095-15dafb58641f">
<img width="1295" alt="Screenshot 2024-04-01 at 12 03 13 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/ea1f2185-6d06-4413-a26c-fb370c58a3ca">

## Part 2: Scrape and Analyze Mars Weather Data
### Step 1
First, I used automated browsing to visit the Mars Temperature Data Site. I inspected the page to identify which elements to scrape. 

<img width="1295" alt="Screenshot 2024-04-01 at 12 06 37 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/080bd499-29db-4d6b-bb43-72f8c0159afc">

### Step 2
Next, I created a Beautiful Soup object and used it to scrape the data in the HTML table. Although I could have used the Pandas read_html function, I opted to continue sharpening my web scraping skills by using Beautiful Soup.

<img width="1295" alt="Screenshot 2024-04-01 at 12 08 30 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/97b14906-e386-4a8c-85d1-3f524290f22a">
<img width="1295" alt="Screenshot 2024-04-01 at 12 08 19 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/f856e6fc-9a7c-4e0d-8350-e235738f7d39">

### Step 3
Next, I assembled the scraped data into a Pandas DataFrame. The columns had the same headings as the table on the website, which included:
* id: the identification number of a single transmission from the Curiosity rover
* terrestrial_date: the date on Earth
* sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
* ls: the solar longitude
* month: the Martian month
* min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
* pressure: The atmospheric pressure at Curiosity's location

<img width="1295" alt="Screenshot 2024-04-01 at 12 10 00 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/203c31dc-4329-41a7-9e93-514e36cd2e09">
<img width="1295" alt="Screenshot 2024-04-01 at 12 10 09 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/d1510e80-0a4f-4195-8693-19193b51f80c">
<img width="1295" alt="Screenshot 2024-04-01 at 12 10 19 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/fe175fe8-694b-4392-aed4-8ddf5af43fb7">

### Step 4
After that, I examined the data types associated with each column. If necessary, I cast (or converted) the data to the appropriate datetime, int, or float data types.

<img width="1295" alt="Screenshot 2024-04-01 at 12 11 34 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/8a2097bc-1f28-4860-a7a8-e733f40ad4ae">
<img width="1295" alt="Screenshot 2024-04-01 at 12 11 45 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/e49286c5-e2c6-4476-825b-de024f5caa14">
<img width="1295" alt="Screenshot 2024-04-01 at 12 11 52 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/b2a320e2-43d2-4001-898b-73b9e7e20347">

### Step 5
Finally I, I analyzed the dataset using Pandas functions to answer several questions:
* How many months exist on Mars.
* How many Martian (and not Earth) days worth of data exist in the scraped dataset.
* The coldest and warmest months on Mars (at the location of Curiosity) by finding the average minimum daily temperature for all of the months and plotting the results as a bar chart.
* Which months have the lowest and the highest atmospheric pressure on Mars by finding the average daily atmospheric pressure of all the months and plotting the results as a bar chart.
* How many terrestrial (Earth) days exist in a Martian year by considering how many days elapse on Earth in the time that Mars circles the Sun once, and I visually estimated the result by plotting the daily minimum temperature.

<img width="1295" alt="Screenshot 2024-04-01 at 12 13 58 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/74754e77-5de7-4ffa-b52e-17eeb05c3b10">
<img width="1295" alt="Screenshot 2024-04-01 at 12 14 16 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/672a2f62-5cdc-4009-ba6e-e3296b33bae3">
<img width="1295" alt="Screenshot 2024-04-01 at 12 14 27 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/8bb58dbc-7c62-4e12-9019-a47ca9d433b8">
<img width="1295" alt="Screenshot 2024-04-01 at 12 14 38 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/b5c27a82-86e3-4d0f-a72e-bb3f0080f1e6">
<img width="1295" alt="Screenshot 2024-04-01 at 12 14 50 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/7e15c249-1163-4273-8e97-3d6425bc3bdf">
<img width="1295" alt="Screenshot 2024-04-01 at 12 15 00 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/f7841760-ab33-4fd4-bce1-f0ffa2c2f371">
<img width="1295" alt="Screenshot 2024-04-01 at 12 15 09 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/32cb5358-9924-4bed-bd4f-210fa5fd5551">
<img width="1295" alt="Screenshot 2024-04-01 at 12 15 19 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/fd2e8465-fa57-4c48-9ab8-450295b57e3c">
<img width="1295" alt="Screenshot 2024-04-01 at 12 15 28 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/8e0b0913-7703-4797-88ba-dcbc002d0b1f">
<img width="1295" alt="Screenshot 2024-04-01 at 12 15 43 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/8ac499d4-8f1f-4ae5-8d81-59fb665f75b6">
<img width="1295" alt="Screenshot 2024-04-01 at 12 15 51 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/5b1d4540-3e84-435b-9476-5d88f30d4f34">

Upon analysis of the data, I was able to conclude that,
1:  There are 12 different months on Mars.
2:  There are 1867 martian days or sols in the scraped data set.
3:  On average, the third month has the coldest minimum temperature on Mars at an average of -83.3 degrees celsius and on average, the eighth month was the warmest with an average temperature of -68.38 degrees celsius
4:  Atmospheric pressure is, on average, lowest in the sixth month at 745.05 units and atmospheric pressure is, on average, highest in the ninth month at 913.30 units.
5:  We can measure the distance between two peaks or troughs to determine an approximate length of a martian year. The distance from the first peak to the second peak is roughly 850-200, or 650 days, so a year on Mars appears to be about 650 days from the plot, an internet search confirms that a Mars year is equivalent to 687 earth days.

### Step 6
Lastly, I exported the DataFrame to a CSV file.

<img width="1295" alt="Screenshot 2024-04-01 at 12 19 33 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/33d21b6f-56e7-4ab7-80b3-f5ff0a3ed0cf">
<img width="1295" alt="Screenshot 2024-04-01 at 12 19 40 PM" src="https://github.com/mattflanagan2/data_scrape_challenge/assets/146908072/9b31da86-c5bc-4386-aabf-9f4715905959">



