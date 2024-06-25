---
created: <% tp.file.creation_date() %>
---
tags:: [[+Daily Notes]]

# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>

<< [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD-dddd').subtract(1, 'd').format('YYYY-MM-DD-dddd') %>|Yesterday]] | [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD-dddd').add(1, 'd').format('YYYY-MM-DD-dddd') %>|Tomorrow]] >>

---
# 📅 Daily routine
### 🛏️ Moring setup
- [ ] <span style="color:#00b0f0">Wake & hydrate</span>
- [ ] <span style="color:#00b0f0">Pushups</span>
- [ ] <span style="color:#00b0f0">10 min Meditate</span>
- [ ] <span style="color:#00b0f0">Morning Plan</span>
- [ ] <span style="color:#00b0f0">Gym</span>
- [ ] <span style="color:#00b0f0">Breakfast</span>

- [ ] Leetcode
- [ ] Daily job


- [ ] <span style="color:#00b0f0">After-work walk & lunch</span>
- [ ] <span style="color:#00b0f0">Church</span>

- [ ] Market analysis
- [ ] Reading
### 🌃 Before sleep
- [ ] <span style="color:#00b0f0">Dinner</span>
- [ ] <span style="color:#00b0f0">Write in Disease Coexistence Journal</span>
- [ ] <span style="color:#00b0f0">10 min Meditate</span>
- [ ] <span style="color:#00b0f0">Pray</span>

---
# 📝 Notes
- <% tp.file.cursor() %>

---
### Notes created today
```dataview
List FROM "" WHERE file.cday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.ctime asc
```

### Notes last touched today
```dataview
List FROM "" WHERE file.mday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.mtime asc
```