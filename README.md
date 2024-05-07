# Managing Large-Scale Website Content and Internal Linking

An overview of how I manage content across a website, visualize internal linking structure, and track keywords in a simple keyword database.
### Context
Efficiently managing internal linking and tracking content across a vast number of blogs on a large-scale website can very quickly become a bit of a nightmare. This complexity often makes it far more difficult to manage the internal linking of the website as the website and it's content continues to scale. 

As a result, I've put quite a bit of thought into finding the best approach to manage and track content and it'd internal linking. My approach has involved lots of refinement over time and as such, is continuing to evolve. This repository contains the latest version of that process. 

Despite it's limitations and clunkiness, I've built out a "Version 1" of this process in a standardized spreadsheet. I have yet to find a tool that covers all the aspects of what I'm aiming to do, but if you happen to find something that checks all the boxes - [someone let me know](https://rkseo.xyz#form).

*I've also got some custom tools I may build some day to remedy the limitations of the ever janky spreadsheet. But until then...* 
## Proposed Solution
I've aimed to create a singular spreadsheet where I can maintain a keyword database and content silos that cover everything I need. Within this I can track current pages, their primary keyword, visualize it's linking structure, and more. I've outlined the core components of this process below.

- Keyword Database: A loosely organized tab with every keyword I've identified as a potential target. Gathered and organized based on my [topic cluster workflow.](https://github.com/krutzar/topic-cluster-creation/) 
- Silo Structure: Organizing published pieces of content into a silo structure to visualize internal linking, and track page & primary keyword performance. 
- Google Search Console Data: I have a tab for pasting in bulk google search console data to run calculations. GSC itself doesn't let you export more than 1000 lines, but you can use Google Looker Studio to get around this. 
## Strategy and Implementation

### Creating an SEO Keyword Database
The keyword database is created throughout my cluster creation process. If you're not familiar with that, I have another repository breaking all of it down. But for the time being, just know that it involves analyzing a large amount of keywords within a certain topic to come up with a giant list of keywords that can then be broken down into silos. 

This keyword database simply acts as an organized version of this initial clustering pass, with a note of what article I am using to tackle a group of keywords within this list. And then I simply pull current rankings. I'm not interested in historical data, not that it wouldn't be nice to have, but I ultimately don't need it all that much, and it's just easier not to track it, given the sheer scale of how much data I would be tracking and managing on a historical level within this spreadsheet.

What's nice about this is that it allows you to easily see how well an article is optimized around a batch of keywords, and make decisions as to whether or not you need to reoptimize around certain keywords, or split keywords off to make a separate article, all at a glance.

![Pasted image 20240502112445](https://github.com/krutzar/managing-website-content-and-internal-linking/assets/28541671/9e9e6c34-1254-430f-91e6-3216989f5193)

If you need more context on how I'm gathering this list, read about my [topic cluster workflow.](https://github.com/krutzar/topic-cluster-creation/) That will explain how I'm gathering and creating this. 
### Silo Structure
My silo structure follow's [Kyle Roof's reverse content silo structure](https://hvseo.co/blog/the-hidden-hero-of-on-page-seo-reverse-content-silos/). Each tier of the silo links to it's neighbors, and up to the parent. I'll also work some links from the parent down into the lower level. 

Here I organize this structure into the primary page, sub-topics, and supporting topics. I make sure to note the URL and it's primary keyword as well. From here I run calculations to grab the most recent ranking for the primary keyword, as well as the total ranking keywords (TRK) for the URL. This lets me see how well a page is preforming overall outside of it's primary keyword. 

Whenever I jump in this spreadsheet after some time has passed, I'll copy and paste values in a previous column and refresh the data. I don't always keep a strict schedule here, but this allows me to have some level of historic data to look back over to see how a rank has changed over time. 

![Pasted image 20240502113253](https://github.com/krutzar/managing-website-content-and-internal-linking/assets/28541671/08069e0b-0788-4031-a8b6-7eacfb8415af)

### Google Search Console Data
In order to run these calculations I like to pull data directly from Google Search Console rather than another tool that tracks rankings, such as Semrush or Ahrefs. While GSC sometimes has some weird data issues (like a keyword seemingly showing up for >10 searches on page one and dropping off - this then counts the ranking as page 1 even though it's not currently there), I find it works best and realistically should be the most trustworthy. 

The hang up however is that GSC only let's you export up to 1000 lines of data directly from the tool. Thankfully you can work around this by creating a table in Google Looker Studio and exporting the GSC data from there. 
![Pasted image 20240502114456](https://github.com/krutzar/managing-website-content-and-internal-linking/assets/28541671/903a6891-52cc-416e-8052-7cb63c1d163c)

By creating two tables - one for query performance and one for URL performance - you can get all the data you need. If you build these tables out you're able to right click and export data to a CSV to be manipulated in Excel. 

### Management and Updating Internal Links
Lastly this brings me to the actual management and updating of the internal links on the website. Tracking whether or not they've actually been done, making sure things are linked together, so on and so forth. 

Unfortunately, right now, this is the biggest weakness in my process, as there is no good way to tell whether or not an article has been linked properly within the spreadsheet. Right now, the way I do it is simply by hand. I only make the internal linking updates for a cluster once the cluster has been fully published. 

Because I'm not able to publish a cluster all at once, I just take the downside of an article initially going live without any sort of internal linking outside of what is already live and able to have been done throughout the outline and writing process. 

I've worked with my team to make sure that we can track a cluster as it goes along, and once it's live, I get notified to go and make all those internal linking updates. And after that, I just make sure not to touch a cluster again. Whenever I refresh a blog, I just make sure to maintain internal links.

In the future I'd like to build some sort of web crawler that can go verify links and help me manage all of that, but at the moment it's just another idea on the to-do list. 
## Results and Insights
- Cluster Approach Case Study (Coming Soon)
### Resources and Links Mentioned
- [Topic Cluster Workflow](https://github.com/krutzar/topic-cluster-creation/) 
- [Google Looker Studio](https://lookerstudio.google.com/)
- [Semrush](https://www.semrush.com/), [Ahrefs](https://ahrefs.com/)
- [Kyle Roof's Silo Structure](https://hvseo.co/blog/the-hidden-hero-of-on-page-seo-reverse-content-silos/)
- 










