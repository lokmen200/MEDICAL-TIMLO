---
tag :favorite
---
# ALL The Learned Lecture
```dataview
Table Module as Subject  , Étudiée as Studied
from "S1/Med" 
where Étudiée = "YES"  
sort rating desc
```

# ANATOMIE The Unlearned Lecture
```dataview
Table Module as Subject  , Étudiée as Studied
from "S1/Med"  
where Étudiée = "NO" 
sort rating desc
```
# Uncreated notes 
```dataview
Table Module as Subject  , Étudiée as Studied
from "S1/Med"  
where  CREATED="NO"
sort rating desc
```

