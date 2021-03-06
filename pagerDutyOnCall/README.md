#PagerDuty On Call
Shows who is on call for all the active Escalation Policies and what services have active incidents. If you click on a service, incident or user it will take you to the corresponding PagerDuty page. If you hit the alt key while you are on the plugin you will get some extra information.

![PagerDuty On Call Screenshot](https://github.com/PedroFuentes/bitbar-plugins/blob/master/images/PagerDutyOnCall_Screenshot.png)

## Installation
### Prerequisites
For the plugin to work you first need a [PagerDuty v2 API key](https://support.pagerduty.com/docs/generating-api-keys#section-generating-an-api-key).

### Step by Step guide
1. [Get the latest version of BitBar](https://github.com/matryer/bitbar/releases). Copy it to your Applications folder and run it - it will ask you to (create and) select a plugins folder, do so.

2. Download the plugin into your BitBar plugins folder

3. Ensure you the plugin has execution rights

 ```console
 chmod +x pagerDutyOnCall.30s.js
 ```

4. Install the required npm dependencies, if you don't have Node.js installed follow [this installation guide](https://docs.npmjs.com/getting-started/installing-node) and after you are done with the installation open your terminal, go to your BitBar plugins folder and then type

 ```console
 echo 'package-lock=false' >> .npmrc && npm install bitbar@^0.3.0 home-config@^0.1.0 node-fetch@^1.5.2 time-ago@^0.1.0
 ```

5. Create the required configuration file on your home directory

 ```console
 nano ~/.bitbarrc
 ```

6. And add the following configuration information, replace {your-company} with the company name that you can see on the url when you are logged-in in PagerDuty and replace {API-Token} with your API token.

 ```
 [pagerdutyoncall]
 api.endpoint=https://api.pagerduty.com
 api.token={API-token}
 api.query=
 style.prefix=
 ```

7. Choose `Refresh` from one of the BitBar menus

## Configuration
Aside of the required Endpoint and API Token you have the following options:

`api.query` (optional) - will filter the available escalation policies by the provided query

`style.prefix` (optional) - will remove the provided prefix from the escalation policy name

##Contributing
If you find a bug or have a feature request please [submit an issue](https://github.com/PedroFuentes/bitbar-plugins/issues/new). If you want to contribute, fork the repo and when ready submit a Pull Request.
