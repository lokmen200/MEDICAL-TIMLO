---
banner: "![[joyce-mccown-IG96K_HiDk0-unsplash.jpg]]"
banner_y: 0.52571
tag :favorite
---
# ALL The Learned Lecture
```dataview
Table Module as Subject  , Étudiée as Studied
from "Med" 
where Étudiée = "YES"  
sort rating desc
```

# ANATOMIE The Unlearned Lecture
```dataview
Table Module as Subject  , Étudiée as Studied
from "Med"  
where Étudiée = "NO" 
sort rating desc
```
# Uncreated notes 
```dataview
Table Module as Subject  , Étudiée as Studied
from "Med"  
where  CREATED="NO"
sort rating desc
```

