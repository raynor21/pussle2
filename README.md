pussle2
=======

Assignment
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
window.onload = fifteen()
 
function fifteen()
{
    $("controls").onclick = shuffle;
     
     
    var puzzlearea = $("puzzlearea").childNodes;
    var square=$("puzzlearea");
    var blank = document.createElement("div");
     
    var id=1;
    var m=0;
    var x=0;
    var y=0;
    var r=3;
     
    for (var i = 3; i < puzzlearea.length; i=i+2)
    {
        puzzlearea[i].className='puzzlepiece';
        puzzlearea[i].id=id+'';
        id+=1;
         
    }
     
     
    puzzlearea[15].appendChild(blank);
    puzzlearea[15].id='16';
     
    for (var t = 0; t < 4; t++)
    {
        for (var l = 0; l < 4; l++)
        {
            y=100*(t);
            x=100*(l);
 
            $(m+"").style.top=y+'px';
            $(m+"").style.left=x+'px';
            //puzzlearea[m].style.top=y+'px';
            //puzzlearea[m].style.left=x+'px';
            //square[m].style.top=y+'px';
            //square[m].style.left=x+'px';
            //this.style.top=y+'px';
            //this.style.left=x+'px';
            m=m+1;
             
            //puzzlearea[r].style.backgroundPosition=-x+"px"+" "+-y+"px";
            r=r+2;
        }
    }
   
     
    //for (var d = 3; d < puzzlearea.length; d=d+2)
    for (var d = 0; d < puzzlearea.length; d=d+1)
    {
        puzzlearea[d].onclick = move;
        puzzlearea[d].onmouseover = moveable;
    }
     
    //puzzlearea[15].appendChild(blank);
    //puzzlearea[15].id='16';
    
};
 
function move()
{
     
    //this.style.top=parseInt(this.getStyle("top"),10) + 100 + "px"; 
    //this.style.left = parseInt(this.getStyle("left"),10) + 100 + "px";
    var a=this.style.top;
    var b=this.style.left;
     
    
}
 
 
 
 
function moveable()
{
   this.addClassName(".movablepiece");
}
 
function shuffle()
{
         
    $("controls").textContent = "Go!";
     
     
}
