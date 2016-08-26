---
layout: post
title: "Eclipse : Maven error - Failure to transfer…"
description: ""
category: quick-fix
tags: [eclipse]
---
Remove all your failed downloads:

```
find ~/.m2  -name "*.lastUpdated" -exec grep -q "Could not transfer" {} \; -print -exec rm {} \;
```

For windows:

```
cd %userprofile%\.m2\repository
for /r %i in (*.lastUpdated) do del %i
```

Then rightclick on your project in eclipse and choose Maven->Update Dependencies.

[来源stackoverflow]  
[http://stackoverflow.com/questions/5074063/maven-error-failure-to-transfer](http://stackoverflow.com/questions/5074063/maven-error-failure-to-transfer)
