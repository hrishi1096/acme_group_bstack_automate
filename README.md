# acme_group_bstack_app_automate

End to end CI triggered automation run for web application testing

This pipeline runs tests on BrowserStack’s Automate, Percy platform along with reports on the Test Observability dashboard. Pretty awesome. :heart_eyes:

# How to run
To run this test suite:
* simply clone the repository
* install the percy client
* set your environment variables and
* fire up the `npx percy exec -- mvn clean test -P bstack-parallel` from the top directory as shown below
```
npm install @percy/cli
export BROWSERSTACK_USERNAME=<username>
export BROWSERSTACK_ACCESSKEY=<accesskey>
export PERCY_TOKEN=<percy_token>
npx percy exec -- mvn clean test -P bstack-parallel

```

It runs the sample test cases on the chosen browser/platform combinations in
parallel on Browserstack automate

# Which browsers/platforms are being used?

It can be seen in the `browserstack.yml` file.
[Plug and play Browserstack SDK](https://www.browserstack.com/blog/introducing-browserstack-sdk/) :rocket:

You can choose to change the choice of browser/platform combinations by specifying different capabilities.

For ease of use: use [Browserstack's capability generator](https://www.browserstack.com/automate/capabilities)


It can also be triggered from the github actions.
Simply go to the "Actions" tab on this repo and trigger a workflow.


**HAPPY TESTING**


