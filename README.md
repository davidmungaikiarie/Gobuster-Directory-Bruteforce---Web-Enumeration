# Gobuster-Directory-Bruteforce---Web-Enumeration

Here's a short note you can add to your GitHub for future reference:

Gobuster Directory Bruteforce - Web Enumeration
Description: Gobuster is a tool used to perform directory enumeration on a website by brute-forcing potential directory or file names using a wordlist. This method helps in discovering hidden pages or endpoints that may not be indexed by search engines.

Command Used:

bash
Copy code
# gobuster dir -u https://codepen.io/ksmithcodepen/project/full/ABJgmr -w /usr/share/seclists/Discovery/Web-Content/common.txt -s "200,204,301,302,307" --status-codes-blacklist ""
Explanation of Parameters:

dir: Specifies that we're performing directory enumeration.
-u https://codepen.io/ksmithcodepen/project/full/ABJgmr: The target URL for enumeration.
-w /usr/share/seclists/Discovery/Web-Content/common.txt: Specifies the wordlist to use for brute-forcing potential directories.
-s "200,204,301,302,307": Specifies the HTTP status codes to include as valid responses.
--status-codes-blacklist "": Disables the default 404 status code blacklist to ensure all results are considered.
What the Command Does:

Brute-forcing: It tests various paths (from the wordlist) on the specified URL.
Filters Responses: The command captures valid responses from the server (status codes like 200, 204, 301, etc.) and skips the ones that return a 404 error (page not found).
Identifies Hidden Directories/Pages: Useful for uncovering hidden or sensitive endpoints on the target site.
Common Results:

200 OK: Directory or page exists.
301/302: Redirection or redirects to another page.
204: No content (valid, but no response body).
307: Temporary redirect.
