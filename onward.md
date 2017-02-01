# Tech for the Next Phase: Monitoring and Access

Even though we're nowhere near done collecting data, events are pushing us to begin thinking about what we do next. We're already seeing changes to government websites, and we need to be able to **monitor them, filter them, understand them and disseminate them.** 

## Monitoring

[Page Freezer](http://www.pagefreezer.com) has generously donated use of their tracking service for the next four years. We are setting up a server which will provide a testbed for their API's and allow us to query changes to individual pages or domains.  We need to familiarize ourselves with the API and write docs that allow organization members to quickly make sense of its most important features.

### Deliverable
* Proof-of-concept code that queries the server and returns human-usable results in tabular form. This can be CSV, HTML, whatever.
* Documentation outlining the main challenges and next steps in this project.

## Filtering

The vast majority of web page changes are of limited interest to us, and so we need to write filters that allow us to prioritize changes. Our analysts are currently drowning in false positives.  Here are some examples:
* a substantial percentage of pages on [climate.nasa.gov](http://climate.nasa.gov) include a `Latest Resources` box on the right-hand side of the main page. Every page that contains this box will be marked as a "changed page" by our version tracking software.  The relevant change can be seen in [this diff](https://gist.github.com/va-client/c25c6def28b760f25e3190b1e986d2e3/revisions) around line `1305`. A simple ad-hoc filter that discards changes from `<aside class='list_view_module'>` would cut out about [30%*](# "Made Up Number.") of our positives from `climate.nasa.gov`. 
* Many domains upate their "Last Updated" date at random. Again, cutting these out would help.
* Other examples? 

### Deliverable
* 2-3 example filters that can be applied to the queries [described above](#monitoring) to improve results. Language and coding practices of the two projects should be compatible
* Documentation suggesting improvements/next steps

## Understanding

This is a very large set of data (10^5 pages already, hopefully 10^6 pages in the future). Most of our analysis team has limited experience extracting semantically relevant information from these kinds of archives. What meaningful information can we expect to find, and what tools will we need to find it?

### Deliverable
* Brief report on appropriate statistical/digital humanities tools for this work. 

## Disseminating
Our work is only relevant if people hear about it. How should we make our work public? What will it take to build public-facing tools to allow citizens to investigate the archive we have assembled?

### Deliverable
* Strategy document for communications and citizen research



