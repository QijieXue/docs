---
layout: home
title: Create Pull Request in Docs Repo
---



<h1>{{page.title}}</h1>

<ul class="list-bus-stop">
 
<li><a href="#01">Content curration</a></li>
<li><a href="#1">Final PR and test</a></li>
<li><a href="#3">#sign-off</a></li>
<li><a href="#4">Merged</a></li>
<li><a href="#5">PR2Master</a></li>
<li><a href="#6">Go Live</a></li>
</ul>

 ## SLA
 Mature content (Content quality meet [Learn quality criteria](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-pull-request-quality-criteria?branch=master))
 
 - Handoff to PDETs for `final PR` at least 5 days before your target publish date(PDETs takes 2 days for internal review, logging bug and to collaborate author for applying fix).
 - `#sign-off` on the PR at least 3 days before your target publish date.

### PDETs `final PR` review
- **Actual cost for PR review (module)**: 1.5 -2 hours  
- **PDETs applying fix directly**: 2.5 hours  
- **PDETs collaborate author applying fix**: 2 days (1 day logging bugs and author applying fix in the night, 2nd day for regress and #sign-off)  

### `#sign-off`
- **Actual cost for PR review (module)**: 2 - 3 hours
- **Resolve feedbacks**: a 2nd day after the `#sign-off`  
- **merge to master**: a 3rd day after the `#sign-off`  
- **merge to live**: a 3rd day after the `#sign-off`  

<a name="01"></a>
## Before creating final pull request(final PR)
click-through the module in git repo to correct things like:
1. Check the files name meet following rules:
- Can **only** contain lowercase letters, numbers, and hyphens. Don't use space or punctuation characters.
- Words and numbers in the file name **must** be separated using hyphens.
- Use no more than 80 characters. ([Words count tool](https://www.lettercount.com/))
- Don't use unnecessary small words, such as a, or, and, the, and in.
- Avoid unapproved or unnecessary acronyms. For Azure specificially, don't use rm or arm as acronyms anywhare in a file name.
2. Check the content of markdown files meet following rules:
- For knowledge check, every question has three options to choose from, one correct, two incorrect.
- For knowledge check, every option has explanation.
- For knowledge check, the content start with `quiz: knowledge check`
- For all content, avoid using unnecessary numbered list, numbered list is used **only when there are sequence among the items.**
- For all content, only H2 and lower headings are allowed, do not allow authors to add H1 headings.
- For all content, all embedded videos must be on RedTiger hosting.

Click-through the module work item to correct things like:
1. Check the summary length is 20-25 words; up to 35 words is acceptable.
2. Check the summary, learning objectieves to avoid using unnecessary numbered list.


<a name="1"></a>
## Create final pull request(final PR) for internal PR review

<a name="pr-patterns"></a>Pull request(PR) patterns:  
`learn-pr` repo:
```url
https://github.com/MicrosoftDocs/learn-pr/pull/{pr#}
```
`learn-m365-pr` repo:
```url
https://github.com/MicrosoftDocs/learn-m365-pr/pull/{pr#}
```

`learn-dynamics-pr` repo:
```url
https://github.com/MicrosoftDocs/learn-dynamics-pr/pull/{pr#}
```

`learn-bizapps-pr` repo:
```url
https://github.com/MicrosoftDocs/learn-bizapps-pr/pull/{pr#}
```
Replace the {pr#} in the patterns, you could get the {pr#} from the _Auto Publishing to Learn_ notification email.  
![get pr# from the build notification email]({{site.baseurl}}/assets/get-pr-from-email.png)

#### Task 1: Create final PR, and tag the author in the work item
1. Create a final PR for internal test.
    - In general, it will overwrite the existing open PR everytime you click the **Publish Module** button in git repo.
    - If you want to start a New PR, just close the existing PR. 
    - Click the **Publish Module** button in git repo.

2. Go to work item.
2. In Discussion tab, add a comment to notify author that the final PR is in iternal review.  
    ![notify author pr is in review]({{site.baseurl}}/assets/lpub-pr-in-review-notify-author.png)

#### Task 2: Run internal PR review, and work with author to fix all.

PR review Test Cases:  
[Content Review](https://microsoftdigitallearning.visualstudio.com/Courseware/_queries/query-edit/66abaade-4bd0-4a6f-9925-22c0982a69dc/)  
[PR review](https://microsoftdigitallearning.visualstudio.com/Courseware/_queries/query/ef3edd45-2929-4886-bda8-87ff622ee002)

#### Task 3: Check-in the Policheck result into git repo _Compliance_Results_ folder.

#### Use general badge or general trophy
If the badge for the module is not available when launching the module, use the general badge.  
"/learn/achievements/generic-badge.svg"

If the trophy for the LP is not available when launching the LP, use the general trophy.  
"/learn/achievements/generic-trophy.svg"

**NOTE**: Make sure to replace the general badge or general trophy as soon as you received the real one.

<a name="3"></a>
### Sign-off


1. Go to the PR, check [Pull request(PR) patterns](#pr-patterns) section.
2. Add comment `#sign-off`.  
    ![sign-off pr]({{site.baseurl}}/assets/lpub-final-pr-sign-off.png)
3. Tag the author in the work item.
    - In the Discussion tab, add a comment to notify author that the final PR is sign-off.  
        ![final pr is sign-off]({{site.baseurl}}/assets/lpub-sign-off-notify-author.png)

<a name="4"></a>
### Merged to Release branch

If the final pr is merged to release branch, (**NOW**, go to <a href="#5">PR2master</a> directly):    
![pr is merged]({{site.baseurl}}/assets/lpub-merged-to-release-branch.png)
1. Go to work item.
2. Tag Ashley that the PR is merged, and it is ready to go live.  
    ![pr go live]({{site.baseurl}}/assets/lpub-pr-merged-notify-author.png)

<a name="5"></a>
### Create a pull request (PR) from Release branch to master

After the final pr is merged:
1. Go to the release branch, by clicking the `to` branch in final pr.  
    ![Go to release branch]({{site.baseurl}}/assets/lpub-release-branch.png)
2. Make sure the release branch is selected, click **Create Pull Request**.  
    ![create pr]({{site.baseurl}}/assets/lpub-release-pr-to-master.png)
3. When the build is green, tag @asajohnson for merge.    
    ![tag Ashley for merge]({{site.baseurl}}/assets/lpub-tag-ashley.png)

### Create a pull request (PR) from master to live
Ashley will do that and let us know when it's live.

<a name="6"></a>
### Content is live


#### Task 1: Verify content is live

Module Url pattern:  
```url
https://docs.microsoft.com/en-us/learn/modules/{module_folder}/
```
Learning Path Url pattern: 
```url 
https://docs.microsoft.com/en-us/learn/paths/{lp_folder}/
```
**NOTE**: Replace the {module_folder} or {lp_folder} with real-folder name.

To verify a **new module** is live:
1. Go to the module metadata file in git repos.
2. Find the real-folder name, which is the `Target folder in github`.
3. Construct the docs url using Module Url pattern and real-folder name.
4. Open the Browser to try access the module using docs url.

**If you could access the module with the docs url, then the module is live.**  
**Else if you get a 404 Error, then the module is not live.**  

To verify an **update module** is live:
1. Go to the module metadata file in git repos.
2. Find the real-folder name, which is the `Target folder in github`.
3. Construct the docs url using Module Url pattern and real-folder name.
4. Open the Browser to try access the module using docs url.
5. In the module page, right-click the page, select View Source.  
    ![view source in html page]({{site.baseurl}}/assets/view-source.png)
6. Select Element -> head -> `<meta name="ms.date" content="10/15/2019" />`  
    ![make sure ms.date value is updated]({{site.baseurl}}/assets/lpub-stage-ms.date.png)

**If the _ms.date_ value is latest, then the module is updated.**  
**Else the module update is not live yet.**  

- Use the same method to verify **a new Learning Path** is live.  
- Use the same method to verify an **update Learning Path** is live.

#### Task 2: Tag the content author in work item
1. Go to work item.
1. In the Discussion tab, add a comment to notify author that the content is live and what the docs url is.  
    ![tag author the content is live]({{site.baseurl}}/assets/tag-author-t-content-live.png)
1. In the *04-Publishing Team Use Only* tab:
    - Fill the **Published Url** with the docs url.
    - Fill the **Release date** with the current date. 
1. In the Discussion tab:
    - Change the **Publish stage** to `4-Shipped`
    - Change the **State** to `Resolved`
