<!-- Saved Game: Subscribe Game (GitHub Ready V2) -->
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Subscribe Game</title>

  <!-- Odometer CSS -->
  <link rel="stylesheet" href="https://github.hubspot.com/odometer/themes/odometer-theme-minimal.css">

  <style>
    body{
      margin:0;
      font-family: Arial;
      background:#0f172a;
      color:white;
      text-align:center;
    }

    .box{
      margin-top:30px;
      padding:20px;
    }

    .title{
      font-size:28px;
      font-weight:bold;
    }

    .sub{
      font-size:18px;
      margin-top:5px;
      color:#a5b4fc;
    }

    .panel{
      margin-top:20px;
      display:inline-block;
      background:#1e293b;
      padding:15px;
      border-radius:12px;
      width:320px;
    }

    button{
      margin:5px;
      padding:8px 12px;
      border:none;
      border-radius:8px;
      cursor:pointer;
    }

    .open{background:#22c55e;color:white;}
    .like{background:#3b82f6;color:white;}
    .dislike{background:#ef4444;color:white;}
  </style>
</head>

<body>

<div class="box">

  <!-- HEADER -->
  <div class="title">OpenAi</div>
  <div class="sub"><strong>0</strong></div>
  <div class="sub">Subscribe</div>

  <!-- VIDEO PANEL -->
  <div class="panel">
    <p>📂V Video Panel</p>

    <p>🎥: <span id="name">Tên video</span></p>
    <p>🎬: <span id="quality">720p</span></p>
    <p>👁️: <span id="view">0</span></p>
    <p>👍🏻: <span id="like">0</span></p>
    <p>👎🏻: <span id="dislike">0</span></p>
    <p>💬: <span id="comment">0</span></p>
    <p>🗯️: Bình luận hay</p>

    <button class="open" onclick="openVideo()">📂V Open Video</button>
    <button class="like" onclick="like()">👍🏻 Like</button>
    <button class="dislike" onclick="dislike()">👎🏻 Dislike</button>
  </div>

</div>

<script>
let view = 0;
let likeCount = 0;
let dislikeCount = 0;

function openVideo(){
  view += Math.floor(Math.random()*15)+1;
  document.getElementById("view").innerText = view;

  let q = ["360p","480p","720p","1080p","4K"];
  document.getElementById("quality").innerText =
    q[Math.floor(Math.random()*q.length)];
}

function like(){
  likeCount++;
  document.getElementById("like").innerText = likeCount;
}

function dislike(){
  dislikeCount++;
  document.getElementById("dislike").innerText = dislikeCount;
}
</script>

</body>
</html>
