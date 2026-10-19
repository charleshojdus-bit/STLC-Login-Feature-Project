# STLC Login Feature Project

A learning project that walks the Standard User Login feature (US-LOGIN-001 / FR-LOGIN-001) through the full Software Testing Life Cycle, from requirement analysis to test closure, against a Postman mock server.

## Description

This project was built to get hands-on with each phase of the STLC and to produce test documentation I wrote myself. The plannned coverage includes, user can log in with valid credentials and is redirected to the main page, and that invalid, blank, and boundary-length inputs are handled correctly.

## Scope

**In scope**

- Login with valid credentials, followed by redirect to the main page
- Minimum-length username, password, and both together
- Maximum-length username, password, and both together
- Invalid username, invalid password, and both together
- Blank username, blank password, and both together

**Out of scope**
- Forgot Username
- Forgot Password
- Account Registration/Sign-up
- MFA
- Account Lockout
- Password Reset
- Functionality after reaching Main Page

**Mock Server Limitations**

- Postman Mock Server is unable to verify username or password on minimum/maximum boundary tests. Mock server is unable to verify redirect on UI to the "Main Page". 

## Tools

- Test tool: Postman (mock server)
- Documentation: Microsoft Word
- AI assistance: ChatGPT
- Testing approach: manual API testing against a mock

## Test Environment

- Postman Mock Server 
- Machine: Dell Latitude 3520
- Operating system: Windows 11
- Environment: Local

## Prerequisites

- Postman installed
- The mock server collection imported and the mock running
- Access to the project documents in this repo

No real passwords or other secrets belong in this repository. Use test data only.

## Setup

1. Install Postman.
2. Review the final evidence document: 

- [Read the final test closure and evidence document](./STLC_Login_Closure_Final_Evidence.docx)

- [View test execution screenshots](./STLC%20Login%20Feature%20Evidence/) 

3. Start the mock server and confirm it is listening.

## How to Run

1. Open the collection in Postman.
2. Follow the API execution procedure and use the request methods, bodies, and test data recorded in the final test closure and evidence document.
3. Record the actual response next to the expected result and mark each case Pass or Fail.

## Test Cases

| ID | Scenario | Expected Result |
|----|----------|-----------------|
| TC-01 | Valid username and password | Valid credentials accepted, user redirected to Main Page |
| TC-02 | Minimum-length username | Valid credentials with 8 character username accepted, user redirected to Main Page |
| TC-03 | Minimum-length password | Valid credentials with 8 character password accepted, user redirected to Main Page |
| TC-04 | Minimum-length username and password | Valid credentials with 8 character username/password accepted, user redirected to Main Page |
| TC-05 | Maximum-length username | Valid credentials with 24 character username accepted, user redirected to Main Page |
| TC-06 | Maximum-length password | Calid credentials with 24 character password accepted, user redirected to Main Page |
| TC-07 | Maximum-length username and password | Valid credentials with 24 character username/password accepted, user redirected to Main Page |
| TC-08 | Invalid username | Login fails with an appropriate error |
| TC-09 | Invalid password | Login fails with an appropriate error |
| TC-10 | Invalid username and password | Login fails with an appropriate error |
| TC-11 | Blank username | Required-field validation appears |
| TC-12 | Blank password | Required-field validation appears |
| TC-13 | Blank username and password | Required-field validation appears | 

- For input data 
- [Read the final test closure and evidence document](./STLC_Login_Closure_Final_Evidence.docx)

- [View Screenshot Evidence](./STLC%20Login%20Feature%20Evidence/)

## Test Results

- Date tested: 10/5/26 - 10/6/26
- Tester: Charlie
- Results: 
- [Read the final test closure and evidence document](./STLC_Login_Closure_Final_Evidence.docx)

- Report on Screenshots: [View Screenshot Evidence](./STLC%20Login%20Feature%20Evidence/)

- Empty-field cases TC-011–TC-013 were executed 10/12/26, after correcting the earlier whitespace inputs. API rejection was verified. Required-field indications, UI validation, and redirect behavior were not verified in the mock environment.

## Documentation

- Test plan
- Detailed test cases
- Login requirements
- Test closure report
 
- [Read the final test closure and evidence document](./STLC_Login_Closure_Final_Evidence.docx)

- [View Screenshot Evidence](./STLC%20Login%20Feature%20Evidence/)

## Known Issues

- The mock server returns fixed responses, so some expected results can only be checked as far as the mock allows. The mock was selected to simplify API execution. It compares the submitted username and password with one hardcoded pair and requires exactly those two JSON fields. A successful response contains a fixed mock token; it does not establish production authentication or session security. The mock has no login UI or redirect behavior.

## Author / Contact

- Name: Charlie
- GitHub: [charleshojdus-bit](https://github.com/charleshojdus-bit)
