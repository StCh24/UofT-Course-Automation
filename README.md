# UofT ACORN Tampermonkey Automatic Course Enrollment

This script is designed to help you log in automatically and enroll the courses that are already in your enrollment cart.

This repository contains two userscripts:

1. **Login Redirect Script** – auto-fills the UofT SSO login form and redirects to the ACORN course page.
2. **Auto Enrol Script** – injects a helper button into ACORN and opens one worker window per course to repeatedly attempt enrollment.
---

## Usage

### In `scripts/utoronto-login-redirect.user.js`

```javascript
let username = "your UTORid",
    password = "password";
```

Replace these placeholders



### In `scripts/utoronto-auto-enrol.user.js`

```javascript
const preferredCourses = [
    "CSC148H1",
    "ECO101H1",
    "MAT135H1",
    "MAT223H1",
    "STA130H1",
],
THINK_TIME = 3000,
MAX_REPEAT = 2,
BASE_URL = "https://acorn.utoronto.ca/sws/#/courses/0";
```

- `preferredCourses`: list of target course IDs

Replace these course IDs
(You must have already added these courses to your enrollment cart)


---

## Installation

### Prerequisites

- Google Chrome or Microsoft Edge
- [Tampermonkey](https://www.tampermonkey.net/)

### Install steps

1. Install Tampermonkey in your browser (recommend using Chrome).
2. Import the zip file.
3. Edit the UTORid & password and course list locally.
4. Make sure both scripts are enabled in Tampermonkey.

---

## Usage

1. Open the UofT ACORN login page.
2. The login script auto-fills the credentials and submits the form.
3. After redirecting to the course page, the auto-enroll script adds the `GOGOGO` button.
4. Click `GOGOGO`.
5. The browser opens one window per course and starts the enroll workflow automatically.


---

## Disclaimer

This repository is provided for code review, documentation, and educational inspection of the original automation logic. Use it at your own risk. The user is responsible for compliance, account safety, and any consequences of running browser automation on university systems.
