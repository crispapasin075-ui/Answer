# Answer
About be my valentine
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine</title>

<style>
  body {
    margin: 0;
    height: 100vh;
    background: #1f245a;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: "Segoe UI", sans-serif;
  }

  .frame {
    background: #f6c1cb;
    width: 450px;
    height: 280px;
    border-radius: 12px;
    padding-top: 25px;
    text-align: center;
    position: relative;
  }

  .frame h3 {
    color: #b11226;
    margin-bottom: 10px;
  }

  .emoji {
    font-size: 80px;
    margin: 10px 0;
  }

  .btns {
    margin-top: 15px;
  }

  button {
    font-size: 15px;
    padding: 8px 16px;
    border-radius: 5px;
    border: none;
    cursor: pointer;
  }

  .yes {
    background: #43a047;
    color: #fff;
  }

  .no {
    background: #e53935;
    color: #fff;
    position: absolute;
  }
</style>
</head>

<body>

<div class="frame">
  <h3>Will you be my Valentine?</h3>

  <div class="emoji">😺💖</div>

  <div class="btns">
    <button class="yes" onclick="accepted()">Yes</button>
    <button class="no" id="noBtn">Really sure??</button>
  </div>
</div>

<script>
  const noBtn = document.getElementById("noBtn");

  noBtn.addEventListener("mouseenter", () => {
    const maxX = 330;
    const maxY = 180;

    const randX = Math.random() * maxX;
    const randY = Math.random() * maxY;

    noBtn.style.left = randX + "px";
    noBtn.style.top = randY + "px";
  });

  function accepted() {
    document.body.innerHTML = `
      <div style="
        height:100vh;
        display:flex;
        align-items:center;
        justify-content:center;
        background:#fce4ec;
        font-size:30px;
        font-family:Segoe UI;
      ">
        💕 YAY! See you on Valentine’s Day 💕
      </div>
    `;
  }
</script>

</body>
</html>
