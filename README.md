let x = 200;
let y = 200;
let xspeed = 6;
let yspeed = 4;
let r = 15;
let rectx = 200;
let recty = 10;
let speed = 4;
let score = 0;
let ai = 0;
function setup() {
  createCanvas(400, 400);
}

function draw() {
  
  background(0);
  
fill("white")
  textSize(22);
text("AI SCORE "+" : "+ai,10,45)
  

  text("SCORE "+" : "+score,10,20);
  rect(mouseX,375,100,15)
  rect(rectx,recty,100,15)
  rectx+=speed;
  ellipse(x,y,r*2,r*2)
  x+=xspeed;
  y+=yspeed;
  if(x>width-r||x<r){
    xspeed=-xspeed;
    }
  if(y>height-r||y<r){
    yspeed=-yspeed;
    }
  if((x>mouseX && x<mouseX+100)&&(y+15>=373)){
    score+=1;
    xspeed*=-1;
    yspeed*=-1;
    }
if(rectx>width-100||rectx<10){
  speed=-speed
  }
    if((x>rectx && x<rectx+100)&&(y+15<=40)){
      ai+=1;
    xspeed*=-1;
   yspeed*=-1;
  }
}
