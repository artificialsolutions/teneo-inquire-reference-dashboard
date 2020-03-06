# Teneo Inquire Reference Analytics Dashboard
This example html page can be used as a reference or starting point to develop web-based analytics Dashboards for Teneo. 

The dashboard contains a login form that allows users to login using their Teneo credentials. After the user is logged in, the following charts are shown:
- A bar chart with the sessions per day
- A pie chart with the most triggered flows
- A clickable word tree based on words that are most frequently used by users
- A sankey diagram that shows the session travel paths 

To draw these diagrams the dashboard uses [Google Charts](https://developers.google.com/chart).

The dashboard is created as single file with minimal styling.

## Prerequisites
Before you can use the dashboard you need to have the following:

### A published solution with data
Conversations that you have with your bot in Try out are not stored in your bot's data repository. Before you can use the dashboard, you should publish your bot and generate data by interacting with your bot online.

### Teneo Inquire URL
The Teneo Inquire URL looks like this: 

```
https://[your_team_name].data.teneo.ai/
```

You should replace `[your team name]` with the name of your team. You can find it in the top right corner when you login to your [Teneo.ai environment](https://www.teneo.ai/manage/environment) in the browser.

### Log Data Source (LDS)
Additionally you need the name of the Log Data Source of your solution. You can find it by opening the [teneo.ai bots](https://www.teneo.ai/manage/bots) page in your browser. The LSD is the last part of the Engine URL of your published solution. For example, if the Engine URL of your solution is url is:

```
https://longberry-xxxxx.bots.teneo.ai/longberry_baristas_5jz1h5hxjb3j0931gx7qxwbns2
```

Then your LDS name would be `longberry_baristas_5jz1h5hxjb3j0931gx7qxwbns2`

## Running the dashboard

You can use the dashboard by opening the InquireReferenceDashboard.html file directly in your browser. However, you will need to pass on the Teneo Inquire URL and the Log Data Source name. You can do that in 2 ways: 

1) by editing the html file, or
2) by providing the details as url parameters

Both options are be outlined below:

### Option 1: edit the html file
- Download the InquireReferenceDashbaord.html
- Open the file in a text editor and edit the lines
    - Line 85: replace `https://your_team_name.data.teneo.ai/` with the Teneo Inquire URL of your solution
    - Line 86: replace `your_lds_here` with the LDS name of your solution
- Save your changes
- Open InquireReferenceDashbaord.html in your browser

### Option 2: provide url parameters
- Download the InquireReferenceDashbaord.html
- Open InquireReferenceDashbaord.html in your browser
- Add the following url parameters at the end of url `?server=your_teneo_inquire_url/&lds=your_lds_name`
    - Make sure you replace `your_teneo_inquire_url` and `your_lds_name` with the appropriate values
- Hit enter or reload the page in the browser

After you login, you should see the graphs generated.
