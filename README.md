# Trip Nimbus

A simple and effective command-line based flight search tool built using Python and the **Amadeus API**. This tool helps users search for real-time flights between two cities and saves the results in a clean, structured Excel file.

This tool evolved from a basic terminal interface into something more practical and user-friendly — all while keeping simplicity and clarity in mind.

---

## Features

- Secure authentication via Amadeus OAuth 2.0
- Search flights based on:
  - Origin and destination (IATA codes)
  - Departure date
  - Travel class (Economy, Premium, Business, First)
- Sort results by: Price, Departure time, or Duration
- Fetch airline names via carrier code
- Export results to Excel for offline use

---

## Why Excel Output?

At first, I displayed all flight results directly in the terminal using the `tabulate` library. While that worked, I quickly realized it wasn’t ideal:

- The formatting wasn’t very clean and often broke depending on terminal size.
- I wanted to align things neatly or center text — but the terminal just wasn’t flexible enough.
- Editing or copying the data from the terminal was annoying.

So I decided to switch the output to **Excel**, and it was a much better choice. Here's why:

- Everyone knows Excel — it's familiar and easy to use.
- Offline access — results are saved permanently and can be viewed later.
- Editable — users can filter, sort, or annotate flight data as they like.
- Clean formatting — with column sizing, bold headers, and aligned text.
- Reusable — perfect for comparing options or sharing with friends/family.

---

## Thoughts on Expanding It

When I first started building this tool, I thought of adding many more options like:

- Entering the number of adults, children, and infants
- Filtering only non-stop flights
- Asking about return flights
- More advanced filters (price range, airline preference, etc.)

But when I tried using it myself, I realized it was annoying to type so many inputs every time in the terminal. The experience wasn't enjoyable. That's when the idea of building a **website** version came to mind.

I wanted to turn this into a proper web app with forms, filters, and a beautiful UI — but I didn’t know how to make websites. I considered copying and pasting the backend code into a Flask or Django app, but it didn’t feel right. I didn’t want to blindly use something I didn’t understand.

Instead, I decided I’d rather **learn how to build websites properly** first. It will take time, especially to make it look good — but I want to do it the right way, not the fast way. So for now, I’ve kept this tool simple and stuck with Excel export.

Still, in the future, I hope to **restart this project**, and write a proper frontend + backend system where users can search flights from a browser without typing anything in the terminal. Maybe even host it online.

---

## Development Journey

This project took me **several weeks** to build — and not just because of the functionality. A big part of the time went into:

- Refactoring and making the code cleaner
- Reducing redundancy
- Improving readability and structure
- Making sure the terminal and Excel output looked neat

I could’ve rushed through it, but I really wanted the result to be something I was proud of. So I kept refining it step by step until it felt right.

---

## Tech Stack

- Python 3.8+
- Amadeus API (test environment)
- Libraries:
  - `requests`
  - `openpyxl`
  - `colorama`
  - `tabulate`
  - `dotenv`

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/viskous/trip-nimbus.git
cd project
```

2. Install required packages:

```bash
pip install -r requirements.txt
```

3. Set up your Amadeus credentials in a `.env` file:

```env
AMADEUS_API_KEY=your_amadeus_api_key
AMADEUS_API_SECRET=your_amadeus_api_secret
```

> Note: You need to sign up at [developers.amadeus.com](https://developers.amadeus.com/) to get your Amadeus API credentials.

---

## Usage

Run the script:

```bash
python project.py
```

Provide required input when prompted:

- From and To (IATA codes)
- Departure Date
- Travel Class
- Sort Option

Flight data will be saved in `flights_result.xlsx`.

---

## Contributing

This project was developed as a solo project. However, feedback is always appreciated.
