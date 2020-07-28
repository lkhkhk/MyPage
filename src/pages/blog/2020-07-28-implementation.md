---
templateKey: blog-post
title: GitFlowDB
date: 2020-07-28T06:25:18.378Z
description: "GitFlowDB : 1. Create Branch(Initilization Branch)"
featuredpost: false
featuredimage: /img/gitflowhlkh-20200706.png
tags:
  - GitFlowDB
---
## 1. Create Branch(Initilization Branch)



<!--StartFragment-->

(J) create \[Create Branch] job; execute job(branch type, branch name, server id)

(G) create branch \[branch name] from \[branch type = hotfix ? master : develop]

(G) checkout \[branch name]

(S) copy & rename \[BranchTemplate] to \[branch name]

(S) copy version file \[branch type = hotfix ? master : develop] to branch

(G) commit & push

(S) scp schema files to database server

(S) scp branch files to database server

(D) initialize database : drop & create database and import schema file

(F) flyway baseline for default

(F) flyway migrate baseline version file

<!--EndFragment-->

``

\[J:Jenkins] \[S:Shell] \[G:Git] \[F:FlyWay] \[D:Database]