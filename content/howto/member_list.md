---
title: "How to add yourself to the member list"
groupByYear: false
showAuthor: true
showTableOfContents: true
authors: 
  - "jpthiele"
date: 2025-05-20
---

## (Optional) install Hugo
This website is build using [*Hugo*](https://gohugo.io) which comes as a single executable,
without the need to install anything else.
This can be very helpful if you want to get a preview of your changes,
especially when cropping/resizing your image.

The first step is to follow the instructions at

{{< button href="https://gohugo.io/installation/" >}}
Install Hugo
{{< /button>}}


## Fork the repository
Go to the [GitHub repository {{<icon "github">}} ](https://github.com/GAMM-AG-RSE-RDM/GAMM-AG-RSE-RDM.github.io) and click on the *Fork* button.

This will add a linked copy of the repository into your 'user space', e.g.<br> github.com/jpthiele/GAMM-AG-RSE-RDM.github.io

## Clone the repository 
On your fork click on the code button and copy the 
SSH link. 
In your terminal/console navigate to a folder where you want to download the repository into and type
```bash
git clone <link> 
```
change into the new folder and switch to a new branch
```bash
git switch --create <branch_name>
```
For *<branch_name>* you can choose whatever makes sense to you, e.g. *member_jpthiele*

If you installed Hugo earlier you can start a local live server by calling
```bash
hugo server
```
The command will rebuild the site on changes,
so you can see directly what happens.

## Add yourself to the list

Start by adding a folder inside *content/members*.
Technically, the name of the folder is not important but it would help us to use a recognizable name
such as your initials and last name or your GitHub user name, etc.


### Add your information 

Inside the new folder add a file *index.md*
and replace the angle brackets with the matching information.

```md 
---
title: "<Your_Name>"
tags: ["RSE","RDM"]
memberships: ["<org_1>","<org_2>"]
country: "<Your_country_of_residence>"
pronouns: "<your_preferred_pronouns>"
externalUrl: "<link_to_your_website>"
showTaxonomies: true
showDate: false
weight: 1
---

```
The two tags are used to show everyone if you are interested in RSE and/or RDM,
if you are only interested in one simply remove the other.<br>
Under *memberships* you can list RSE or RDM related organizations 
that you are a member of.<br>
We would like to have an overview on which countries are represented in our group,
so please add your country of residence.<br>
You can also list the gender pronouns you prefer,
but we don't expect you to, so feel free to delete that line.


As an example my *index.md* looks like this:

```md
---
title: "Jan Philipp Thiele"
chair: "Chair"
tags: ["RSE","RDM"]
memberships: ["DE-RSE","GAMM"]
country: "Germany"
pronouns: "he/him"
externalUrl: "https://github.com/jpthiele"
showTaxonomies: true
showDate: false
weight: 0 # so the chairs are up front
---
```

### (Optional) Add an image of yourself.

{{< alert >}}
**Only use an image for which you have the proper usage rights!**
{{</ alert >}}

There are two option for adding the image

1. Add a link to the image by adding the parameter
   ```md
   featureimage: "<URL>"
   ```
   inside *index.md*, but **before** the second set of three dashes
   
2. Add an image file named *featured.jpg* or *featured.png* inside your member folder.


## Commit & Push changes and open a pull request

Just in case, type
```bash
git branch
```
and make sure that you are not on the main branch,
but on a different branch, e.g. *member_jpthiele*


Add the newly created member folder and commit your changes, e.g.
```bash
git add content/members/jpthiele
git commit -m "[Members] add Jan Philipp Thiele"
```
The *[Members]* start of the commit message helps us
with keeping track, so please use it.

Once done you have to push your branch to your fork
```bash
git push -u origin member_jpthiele
```
To open the pull request directly you can click on the link in the command output.


## Don't forget to join the mailing list

To keep up to date with discussions you should also

{{< button href="https://www.listserv.dfn.de/sympa/subscribe/gamm-rse%2Brdm">}}
Join the GAMM RSE & RDM mailing list
{{</ button >}}

if not done already.

## Anything unclear?

If yes feel free to reach out, e.g. by [*opening an issue*{{<icon "github">}}](https://github.com/GAMM-AG-RSE-RDM/GAMM-AG-RSE-RDM.github.io/issues/new) 
and do feel free to ping me by adding @jpthiele to the issue.
