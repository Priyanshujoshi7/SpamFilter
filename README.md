Spam Filter Project

Overview
This project demonstrates the use of regular expressions (regex) to detect potential spam messages by matching patterns in text. Regular expressions are powerful tools that allow programmers to search for and manipulate strings based on specific patterns, making them ideal for filtering out spam in applications like email or chat systems.

In this project, you’ll learn about various regex techniques, including capture groups, positive lookaheads, negative lookaheads, and character classes to accurately detect and block spammy phrases or patterns.

Key Features:

Detects common spam keywords and phrases like:
Requests for help (e.g., "please help", "assist me")
Dollar amounts (e.g., "$100 dollars", "2000 dollars")
Free money offers (e.g., "free money", "fr33 mon3y")
Stock alerts (e.g., "stock alert")
Customized "dear" spam pattern (e.g., "d3ar", "d34r", "d|ar")

Technologies Used:

JavaScript
HTML/CSS (for the interface)
Regular Expressions (Regex)

Regex Techniques Covered:
Character Classes: Match a specific set of characters (e.g., [3e] matches either "e" or "3").
Capture Groups: Group parts of a regex to extract and work with (e.g., (pattern)).
Positive Lookaheads: Assert that a certain pattern exists after the current match (e.g., (?=pattern)).
Negative Lookaheads: Assert that a certain pattern does not exist after the current match (e.g., (?!pattern)).
Matching Whole Words: Ensures regex matches only whole words using boundaries like \b or alternatives.

Regular Expressions Used:

helpRegex: Detects phrases like "please help" or "assist me".



const helpRegex = /please help|assist me/i;
dollarRegex: Matches dollar amounts with optional suffixes (e.g., "100 dollars", "5 million dollars").

const dollarRegex = /[0-9]+\s*(?:hundred|thousand|million|billion)?\s+dollars/i;
freeRegex: Matches patterns like "free money" (with variations like "fr33 mon3y").


const freeRegex = /(?:^|\s)fr[e3][e3] m[o0]n[e3]y(?:$|\s)/i;
stockRegex: Detects stock alerts (e.g., "stock alert", "st0ck al3rt").


const stockRegex = /(?:^|\s)[s5][t7][o0]ck [a@4]l[e3]rt(?:$|\s)/i;
dearRegex: Matches variations of "dear" (e.g., "d3ar", "d|ar", "d34r").


const dearRegex = /(?:^|\s)d[3e][4a][r1|i](?:$|\s)/i;
