> [!IMPORTANT]
> This project has been retired and archived  
> If there is a need of continued use / development of this project for your own needs please feel free to fork the project - which will remain here in archived form.

The Teneo Google Charts dashboard is an example page that can be used as a reference or starting point to develop web-based analytics dashboards for Teneo. 

The dashboard contains a login form that allows you to login using your Teneo credentials. After you are logged in, the following charts are shown:
* A bar chart with the number of sessions per day.
* A pie chart with the most popular flows.
* A clickable word cloud, based on words that appear most frequently in user inputs.
* A sankey diagram that shows the session travel paths.

To draw the diagrams, the dashboard uses [Google Charts](https://developers.google.com/chart).

The dashboard is created as a single HTML file with minimal styling that can be downloaded and opened in a browser.

## Prerequisites
Before you can use the dashboard you need to have the following:

### A published solution with data
Conversations that you have with your bot in Try Out are not stored in your bot's data repository. Before you can use the dashboard, you should publish your bot and generate data by interacting with your bot online. Also make sure that you start the Teneo server by logging into Teneo Studio.

### Teneo Inquire URL
The Teneo Inquire URL looks like this: 

```
https://[your_team_name].data.teneo.ai/
```

You should replace <mark>[your team name]</mark> with the name of your team. You can find it in the top right corner when you log in to your environment in the browser.

### Log Data Source (LDS)
Additionally, you need the name of the Log Data Source of your solution. You can find it by opening the bots page in your browser. The LDS is the last part of the Engine URL of your published solution.


For example, if the Engine URL of your solution is:

```
https://longberry-xxxxx.bots.teneo.ai/longberry_baristas_5jz1h5hxjb3j0931gx7qxwbns2
```

Then your LDS name would be <mark>longberry_baristas_5jz1h5hxjb3j0931gx7qxwbns2</mark>

## Opening the dashboard
You can use the dashboard by opening the [one of the dashboards](https://github.com/artificialsolutions/teneo-inquire-reference-dashboard/releases) file directly in your browser. However, you will need to pass on the Teneo Inquire URL and the Log Data Source name. You can do that in one of two ways: 

* By editing the HTML file.  
* By providing the details as URL parameters.

Both options are outlined below.

Please note that there is a different html file depending on which version of Teneo you are using. 

### Option 1: edit the HTML file
The first option needs the user to edit the HTML file directly by doing the following, 

1. Download the latest version of the dashboard from [github](https://github.com/artificialsolutions/teneo-inquire-reference-dashboard/releases) by clicking the <mark>Source code (zip)</mark>.
2. Unzip the downloaded file.
3. Open the file <mark>InquireReferenceDashboard.html</mark> in a text editor and edit the following lines:
* Line 85: replace <mark>https://your_team_name.data.teneo.ai/</mark> with the Teneo Inquire URL of your solution.
* Line 86: replace <mark>your_lds_here</mark> with the LDS name of your solution.
4. Go ahead and save your changes.
5. Open file <mark>TeneoGoogleCharts-t.html</mark> in your browser.

### Option 2: provide URL parameters
The second option is to prove the LDS and Inquire parameters in the URL, by doing the following. 
1. Download the latest version of the dashboard from [github](https://github.com/artificialsolutions/teneo-inquire-reference-dashboard/releases) by clicking the <mark>Source code (zip)</mark>.
2. Unzip the downloaded file.
4. Open the file <mark>TeneoGoogleCharts-t.html</mark> in your browser.
5. Add the following URL parameters at the end of the URL: `?lds=your_lds_name&server=your_teneo_inquire_url`.
* Make sure you replace <mark>your_lds_name</mark> and <mark>your_teneo_inquire_url</mark> with the appropriate values.
6. Hit enter or reload the page in the browser.


## Log in and view the dashboard
Once you have the dashboard opened in the browser you will be greeted with a very simple login page.
1. Login to the page by using the same credentials as done for Teneo Studio.
It will now take some time to load the data depending on how much it needs to go through.
2. After you log in, you should see the newly generated graphs.

It is possible to add more graphs in the webpage by editing the <mark>TeneoGoogleCharts-t.html</mark> file.
