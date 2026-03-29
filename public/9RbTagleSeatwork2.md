# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<your names>" />
  <meta name="revised" content="<date today>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

> From this, the position of the sidebar goes more to the left or it would overlap the main content area, depending on the value you put in the corresponding positions. For example, when you make the left position bigger, it goes more to the left. 

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

>I don't think anything different is happening when I scroll the page. The footer's position is fixed because it is relative to the viewport.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

>The element sticked to its ancestor. While the fixed's reference point is the view port, the relative's reference point is the ancestor.

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?
> It is because the z-index value determine the layer or the overlapping of the elements present. A higher z-index indicates a higher status, meaning it goes over a lower z-index value. So, in the page, the one with the higher z-index OVERLAPS the one with the lower z-index.
- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    

    >To position the .notice box on the top right corner of the .content box, you first have to put or nest it .notice inside .content in the HTML part. Then, you have to change the position of .content to relative so it becomes the positioning parent. Furthermore, you can also make the values of top and right css of .notice to snap to the top-right corner of .content.


    * Try to change the position of .content to relative then to fixed. What do you observed each time?

    >When the position is relative, the relative position is based on the top and left values. However, even if you scroll, the space is still reserved by the browser and it still flows with the rest of the elements. If it is fixed on the otherhand, it it somewhat locked on the screen. It says put like a floating browser no matter how far you scroll.


    * What do you observe on about the effect of z-index on .notice and .content boxes?

    >As we have stated before, the z-index determines the stacking order of elements, or rather, how they appear on the browser. A higher z-index indicates that is is closest to the viewer. Since .notice has a z-index of 2 and .content has a z-index of 1, .notice is on top of .content whenever they overlap. This means that .notice is visible above .content.



3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    > Position static is the default html positioning method while position relative's reference point is its normal position in the document flow. Position absolute is placed near the nearest positioned ancestor and position fixed's reference point is the viewport.

    b. How does absolute positioning depend on its parent element?

    >It is placed to its nearest ancestor element. 
    

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    >Sticky and fixed are very different from each other. Fixed, from its name, is stuck on the viewport while sticky is sticks to its threshold while an individual is scrolling.

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.

    >I think using position sticky would be the best option as while an individual scrolls, something important---perhaps an event---would be displayed on the user's screen while they are reading the details of an event.