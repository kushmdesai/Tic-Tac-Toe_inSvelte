<h1>This is a website</h1>
<p>Visit <a href="https://www.github.com/kushmdesai/" target="_blank" rel="noopener noreferrer" >my github repo</a> to see the code</p>
<br>
<script>
  let board = Array(9).fill(null);
</script>

<style>
    a:hover {
        color: #0000ff;
    }
   .container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
   } 
  .board {
    display: grid;
    grid-template-columns: repeat(3, 100px);
    grid-template-rows: repeat(3, 100px);
    gap: 5px;
  }

  .cell {
    background-color: #eaeaea;
    border: 5px solid #000;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    cursor: pointer;
    transition: transfrom 0.5s ease, background-color 0.5s ease;
  }
  .cell:hover {
    transform: scale(1.2);
    background-color: #ff0000;
  }
  :global(body) {
  background-color: #f4ecd8;  /*aged paper color if png does not work*/
  background-image: url(https://t3.ftcdn.net/jpg/03/66/10/14/360_F_366101427_8yazUJK82fDrLi4YtpnQO3DJ4dTygxoe.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-attachment: fixed;
  background-size: cover;
  margin: 0;
  overflow:hidden
}
</style>
<div class="container">
    <div class="board">
        {#each board as cell}
            <div class="cell">
            {cell}
            </div>
        {/each}
    </div>
</div>
