---
<%*

    let title = tp.file.title

    if (title.startsWith("Untitled")) { title = await tp.system.prompt("Title");

    await tp.file.rename(`${title}`); }

%>
Date created : <%tp.date.now("YYYY-MM-DD")%>
Date of last modefiction : <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm") %>
Module : <%tp.system.suggester(['ANATOMIE' , 'EMBRYOLOGIE' , 'CYTOLOGIE' , 'BIOCHIMIE','BIOPHYSIQUE','CHIMIE','BIOSTAT','HISTOLOGIE','PHISOLOGIE'],['ANATOMIE' , 'EMBRYOLOGIE' , 'CYTOLOGIE' , 'BIOCHIMIE','BIOPHYSIQUE','CHIMIE','BIOSTAT','HISTOLOGIE','PHISOLOGIE'])%>
Cour : <%* tR += `${title}` %>
Present dans le coure : <% await tp.system.suggester(["Present dans l'amphi" , 'NO pas present'],['YES' , 'NO'])%>
Étudiée : <%tp.system.suggester(["LEARNED", "NOT LEARNED YET"],['YES' ,"NO"])%>
tag: 
CREATED: <% await tp.system.suggester(["NOTE CREATED" , 'NOTE NOT CRETED'],['YES' , 'NO'])%>
QCM: <% await tp.system.suggester(["QCM SOLVED" , 'QCM NOT SOLVED YET'],['SOLVED' , 'NOT YET'])%>
cards-deck: <%tp.file.folder(true)%>::<%* tR +=`${title}` %>
---

```toc
```