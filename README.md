# Renovate-testing

how did you install it?
while installing, it asks for do you want to enable it for all repo or a specific repo? Which one did you select?
dashboard renovate ka

Go to https://github.com/apps/renovate -> Install
It will asks for do you want to enable it for all repo or a specific repo? Say specific repo. 

To confirm, it is installed or not, Org ki settings -> Applications -> You will see Renovate would have come now.

https://developer.mend.io/github/sonali-varshney - ye dashboard h renovate ka

if yoyu want to change the repo or add a new repo to renovate , go to https://github.com/apps/renovate -> configure
																	 OR  Org ki settings -> Applications -> Renovate -> configure
																	 
Jo bhi repo select krenge vo reflect kregi renovate dashboard me -> click on that repo -> you will see renovate ka status us repo pr(Running/Completed/Done)

lets go to repo -> PR -> Renovate already 1 PR bna dega.. ye onboarding PR hoga.. Isme agr hm jae Files changed wale tab me , we will see renovate.json file bnai hogi Renovate ne..basically isne 1 branch bnai us branch me ye add kr rha h is file ko basically main branch me through PR. To activate Renovate, merge this Pull Request.Lets merge this PR.

renovate.json ka content h:
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "config:recommended"
  ]
}

merge krne pr ye renovate.json hmari repo k root me aa jaegi

we can modify this renovate.json file acc to our need.

When you merge this PR, you go to Issues tab, you will see it creates a dashboard for your repo. 


create a file say package.json usme purani dependency likhi ->  Renovate automatically PR raise krega -> dependency update kr dega.. if you will open the PR, it will show below thing 

This PR contains the following updates:

Package					Change			Age		Confidence
lodash (source)		4.17.15 → 4.17.23		54d		High

is k niche release notes bhi dikhaega ki kya change h dependency k is new version me. you cn go ahead and merge PR.

***************************
agr pom.xml me say 2 dependency h jo update honi h so 2 PR raise honge, 1 package.json me say 1 dependency h jo update honi h so 1 PR raise hoga..so total 3 PR raise hue. So lets say 100 dependencies update honi h so 100 PR raise honge.. So better , use grouping feature of renovate . PR ko group kr skte ho on the basis of major/minor/patch, 

Issues tab me ja k dekho dashboard renovate ka aisa aega

Open
The following updates have all been created. To force a retry/rebase of any, click on a checkbox below.


Update dependency lodash to v4.17.23

Update dependency org.apache.commons:commons-lang3 to v3.20.0

Update dependency org.springframework.boot:spring-boot-starter-web to v2.7.18

Click on this checkbox to rebase all open PRs at once
Detected Dependencies
maven (1)
npm (1)

************
