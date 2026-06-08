# check_internet

Use this tool whenever the user asks to check, test, or verify if the AI or system has active internet access. This tool fetches data from a public API.

## Script

```javascript
(async () => {
    try {
        const res = await fetch('[https://api.ipify.org?format=json](https://api.ipify.org?format=json)');
        const data = await res.json();
        return "Internet status: Connected. Data: " + JSON.stringify(data);
    } catch (err) {
        return "Internet status: Disconnected/Blocked. Error: " + err.message;
    }
})();
