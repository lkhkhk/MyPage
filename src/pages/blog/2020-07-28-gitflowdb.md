---
templateKey: blog-post
title: GitFlowDB
date: 2020-07-28T06:40:22.830Z
description: "GitFlowDB : 2. Migration Branch(auto)"
featuredpost: true
featuredimage: /img/gitflowhlkh-20200706.png
tags:
  - GitFlowDB
---
<!--StartFragment-->

# 2. Migration Branch(auto)

<!--EndFragment-->

<!--StartFragment-->

(J) create \[Migration Branch]job; execute job(branch name, server id)

(G) checkout \[branch name]

(S) scp branch files to database server

(F) flyway migrate branch files

<!--EndFragment-->

<!--StartFragment-->

\[J:Jenkins] \[S:Shell] \[G:Git] \[F:FlyWay] \[D:Database]

<!--EndFragment-->