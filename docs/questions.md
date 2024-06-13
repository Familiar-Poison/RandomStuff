### What exactly happens when a browser tries to access a website?

##### 1. URL Entry and DNS Resolution
* **User Input:** The user types a URL into the browser's address bar
* **DNS Lookup:** The browser checks it cache for the IP address associated with the domain name. If not found, it queries the DNS server to resolve the domain name into an IP address.

##### 2. Establishing a Connection
* **TCP/IP Connection:** THe browser establishes a TCP connection to the server using the resolved IP address. This involves a three-way handshake (SYN, SYN-ACK, ACK).
* **SSL/TLS Handshake (if HTTPS):** If the website uses HTTPS, an SSL/TLS handshake occurs to establish a secure connection. This involves exchanging certificates and encryption keys.

##### 3. Sending an HTTP Request
* **HTTP Request:** The browser sends an HTTP request to the server. This includes details such as the method (GET, POST, etc.) headers, and optionally, a body (for methods like POST).

##### 4. Server Processing
* **Server Receives Request:** The server processes the request, checking for the requested resource ( web page, image or API endpoint).
* **Server Response:** The server generates an HTTP response, including status code (200 OK, 404 Not Found, etc.), headers (content type, length, etc.), and the response body (HTML, CSS, JavaScript, images, etc.).

##### 5. Receiving and Rendering the Response
* **Receiving the Response:** The browser receives the server's reponse. It reads the status code and headers to understand how to process the response body.
* **Rendering the Content:** 
    * **HTML Parsing:** The browser parses the HTML content and constructs the DOM (Document Object Model) tree.
    * **CSS Parsing:** CSS files are fetched and parsed to apply styles to the HTML elements.
    * **JavaScript Execution:** JavaScript files are fetch and executed. This can modify the DOM and CSSOM (CSS Object Model).
    * **Layout and Painting:** The browser calculates the layout of the elements and paints them onto the screen.
##### 6. Fetching Additional Resources
* **Resources Requests:** As the HTML is parsed, the browser identifies additional resources (CSS, JavaScript, images, fonts, etc.) and sends HTTP requests for these resources.
* **Rendering Updates:** As additional resources are loaded and executed, the browser may need to re-render parts of the page.

##### 7. User Interaction and JavaScript Execution
* **Event Handling:** The browser handles user interactions (clicks, inputs, etc.) and JavaScript events, dynamically updating the page as needed.
* **Asynchronous Requests:** JavaScript can make asynchronous HTTP requests (AJAX, Fetch API) to load additional data without refreshing the page. 

### Scenario Questions

##### 1. A bash script that executes daily suddenly fails. The bash script was previously working with no changes and it's only function is to transfer files from a local drive to a network drive. 

* **Check for Errors in the Script**
    * Run the script to manually to see if any error messages are displayed. This can give you a clue about what might be going wrong.

        ```
        /path/to/your/script.sh
        ```

* **Check Logs**
    * If your script writes to a log file, check the log for any error messages or unusual entries. If it doesn't, consider adding logging to capture what happens during execution.

* **Check Network Connectivity**
    * Since your script transfer files to a network drive, ensure that the network connection is stable and the network drive is accessible.

* **Verify Permissions**
    * Ensure that the script has the necessary permissions to access both the source and destination directories.

        ```
        ls -l /local/directory/
        ls -l /network/directory/
        ```

* **Check Disk Space**
    * Ensure that there is enough disk space on both the local drive and the network drive.

        ```
        df -h /local/directory/
        df -h /network/directory/
        ```

* **Check for System Changes**
    * Determine if any system changes occurred around the time the script started failing, such as updates, configuration changes, or changes to the network environment.

* **Review Crontab Entry**
    * If the script is scheduled via **cron**, verify that the crontab entry is correct and hasn't been altered.

        ```
        crontab -l
        ```
* **Check for Environmental Changes**
    * Ensure that the environment in which the script runs (e.g, environment variables, PATH) hasn't changed.

* **Increase Script Debugging**
    * Enable debugging in your script to get more detailed output during execution.
        * Add the following to the top of your script to print each command and its argument as they are executed.

            ```
            set -x
            ```




---

##### [Back to Main](./index.md) 