# champions
Script to process Champions League

How to parse BeautifulSoup
list(soup.children)
[type(item) for item in list(soup.children)]
html = list(soup.children)[2]
list(html.children)
body = list(html.children)[8]

list(s.children)[1] = top box score
  list(s.children)[3] = Gridiron Dynasty ad
  list(s.children)[5] = Score Summary
  list(s.children)[7] = Just the table header for 'Team Statistics'

list(soup.children)[2] = Top Box Score, Scoring Summary, Table Header for "Team Statistics"
  list(s.children)[1] = top box score
  list(s.children)[3] = Gridiron Dynasty ad
  list(s.children)[5] = Score Summary
  list(s.children)[7] = Just the table header for 'Team Statistics'

list(soup.children)[3].get_text() = away team: Year, Team, Mascot
list(soup.children)[4].get_text() = home team: Year, Team, Mascot

list(soup.children)[6] = Team Stats, First Downs
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[8] = Team Stats, First Downs, Rushing
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[10] = Team Stats, First Downs, Passing
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[12] = Team Stats, First Downs, Penalty
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[14] = Team Stats, Third Down Efficiency
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[16] = Team Stats, Fourth Down Efficiency
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[18] = Team Stats, Rushes-Yards
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[20] = Team Stats, Avg Rush
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[22] = Team Stats, Comp-Att-Int
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[24] = Team Stats, Passing Yards
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[26] = Team Stats, Sacks-Yards
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[28] = Team Stats, Fumbles-Lost
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[30] = Team Stats, Punts-Avg
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[32] = Team Stats, KR-Avg
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[34] = Team Stats, PR-Avg
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[36] = Team Stats, Penalties-Yard
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[38] = Team Stats, Time of Possession
  list(a.children)[1].get_text() = Category
  list(a.children)[3].get_text() = Away 
  list(a.children)[5].get_text() = Home 

list(soup.children)[44] = Player Stats
   list(a.children)[1] = Next Step
     list(n.children)[1] = Rushing Stats Table
       list(r.children)[1] = Away Wrapper
         list(b.children)[1] = Away Wrapper 2
           list(c.children)[1] = Table Header
           list(c.children)[3] = Players
Formula:    len(list(c.children)[3]) / 2 - 0.5 =  of players in stat table
             list(d.children)[X] = X Player's Stats
Formula:      len(list(e.children)[X]) / 2 - 0.5 =  of stats in stat table
Formula:      for i in range(len(list(e.children)[X]) / 2 - 0.5):
                  dataFrame.append(list(e.children)[i * 2 - 1]))
               list(e.children)[1] = Year + Player

Formula:          Replaces the html character for a space in the player's name
                  name = ""
                  name = str(list(f.children)[1].get_text())
                  name.replace(r"\xa0", " ")

               list(e.children)[3] = Att
               list(e.children)[5] = Yds
               list(e.children)[7] = 20+
               list(e.children)[9] = L
               list(e.children)[11] = TD
Formula:         str(list(f.children)[0]) = Text Value


       list(r.children)[3] = Home Wrapper

     list(n.children)[3] = Receiving Stats Table


     list(n.children)[5] = Passing Stats Table


     list(n.children)[7] = Defense Stats Table


     list(n.children)[9] = Field Goal Stats Table



list(soup.children)[48] = Player of the Game
  list(a.children)[1] = Wrapper
      list(b.children)[1] = Title
      list(b.children)[1] = Player
        list(c.children)[0] = Wrapper
          list(d.children)[0] = Wrapper
Formula:    name = str(e)
            name = name[:(name.find("(") - 1)]



This gets you the plain text version of the lowest element
x.get_text()
