---
<%* 
	let title = tp.file.title 
	if (title.startsWith("Untitled")) { title = await tp.system.prompt("Title"); 
	await tp.file.rename(`${title}`); }
%>
Date created : <%tp.date.now("YYYY-MM-DD")%>
Date of last modefiction : <% tp.file.last_modified_date("dddd Do MMMM YYYY") %>
chaptire numbre : <% tp.system.prompt("Chapitre order : ", ) %>
name of the chaptire : <%* tR += `${title}` %>
Finished : <% await tp.system.suggester(["NOT YET" , 'finished'],['YES' , 'NO'])%>
tag: <% tp.system.prompt("TAGS : ", ) %>
---
# <%* tR += `${title}` %>
<% tp.file.cursor()%>