---
cover:
description: Now that you have learned how to create a postmortem, let's take a look at how to create one in the PagerDuty application.
---
![Next Steps](../assets/img/headers/Postmortems-NextSteps.png)
## Create a Report in PagerDuty

If you are using PagerDuty for incident management, we strongly encourage you to take advantage of our postmortems feature. This allows you to associate incidents and other data within PagerDuty with your report, which will help with timeline generation and allow you to write a more comprehensive report. Note that only non-stakeholders can create, modify, and/or delete postmortems. (For a matrix of user permissions, please see our [support page](https://support.pagerduty.com/docs/user-roles) and refer to the postmortems line items.)
### Create the Report

To create a postmortem from an incident, you can select the (resolved) incident and click the New Postmortem Report button:

![Create a New Report Option 1](../assets/img/thumbnails/NextSteps/1NewPostmortemReport.png)

Alternatively, you can create a postmortem from the catalog, by either going to Incidents -> Postmortems or directly to `yoursubdomain.pagerduty.com/postmortems`. From there, you click New Report:

![Create a New Report Option 2](../assets/img/thumbnails/NextSteps/2NewPostmortemReport.png)

If you're creating a postmortem report from the catalog, you'll need to associate the incident after you start the report. If you include the estimated start and/or end times, the PagerDuty app will limit the possible incidents associated with that report to incidents that happened in that timeframe. 

![Data Sources](../assets/img/thumbnails/NextSteps/3PostmortemDataSources.png)


Regardless of whether you created a report from an incident or the catalog, you can add additional incidents using the timeframe or incident number for situations where multiple incidents apply to a single report.

The PagerDuty app will create a timeline to appear in the postmortem based on the in-app events:

![Create Timeline](../assets/img/thumbnails/NextSteps/4CreateTimeline.png)

If you have integrated with Slack or another data source, that information will also appear in the Available Data on the left. You can choose which items to add or remove using the arrows in the center.

After you've completed the timeline, you will need to write in the Analysis. This section has several subsections. Some of the default subsections are Overview, What Happened, and Resolution:

![Postmortem Details](../assets/img/thumbnails/NextSteps/5PostmortemDetail.png)

Once you have the information you would like in the report, click Save & View Report. This will save the report in the Draft state (the report will also autosave in the Draft state). The states available for the postmortem report are: Draft, In Review, Reviewed, and Closed. You can edit the status by clicking on the report from the Postmortem Catalog and using the Status drop down menu, which is located at the top of the page:

![Change Postmortem Status](../assets/img/thumbnails/NextSteps/6ChangePostmortemStatus.png)

## Addenda
### External Access 
You can export your postmortem report to a PDF at any stage. This is primarily used if there are reviewers not in the PagerDuty app or if there is a different, centralized tool for the company for others to view the final report. To save as a PDF, simply select the report from the Postmortem Catalog and click the Save as PDF button:

![Export Postmortem to PDF](../assets/img/thumbnails/NextSteps/7ExportPostmortemPDF.png)

### Customizations
We strongly recommend that you modify the default report template to fit your company's needs. This can involve adding or removing sections, changing wording to match common language, or modifying the clarifying text in each section so that it communicates what is needed.

If you would like to add, edit, or remove sections you can do so under Settings in the Postmortem Catalog:

![Edit the Postmortem Template](../assets/img/thumbnails/NextSteps/8EditPostmortemTemplate.png)

You can Edit sections by clicking on the gear for the appropriate section. You can also click Add Section at the bottom of the template to add a completely new section:

![Edit Postmortem Section Text Areas](../assets/img/thumbnails/NextSteps/9EditPostmortemSections.png)

Changes will only apply to postmortem reports moving forward—they will not apply to reports that have already been created.
For some guidance for what questions and clarifying information to put on your questions, take a look at the [Analysis Questions section](https://postmortems.pagerduty.com/resources/analysis/) under the Resources for this guide.

If at any point you'd like to start again from the default template, you can reset the template. To revert to the original default sections, click on the Reset Template button at the top of your Report Template. You will be prompted in a pop-up menu to Reset Template or Cancel.

### Navigating Between Reports and Associated Incidents
Currently, the only way to see an incident associated with a report is to open the report and look at the incidents that have been added to it. You cannot currently view a report by navigating to an incident to see an associated report.
