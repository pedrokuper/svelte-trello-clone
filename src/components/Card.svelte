<script>
  const tags = ["Bug", "Fix", "Falopa"];
  const users = [
    "https://thispersondoesnotexist.com/",
    "https://thispersondoesnotexist.com/",
  ];
  const title = "Card Title";
  const date = "28 Sept";
</script>

<div class="card">
  <ul>
    {#each tags as tag}
      <li>{tag}</li>
    {/each}
  </ul>
  <h5 class="card-title">{title}</h5>
  <div class="card-lower">
    <div class="card-details">
      <span class="card-date">{date}</span>
      <span class="card-task">tasks 0/3</span>
    </div>

    <div class="card-user">
      {#each users as user}
        <img src={user} alt="" />
      {/each}
    </div>
  </div>
</div>

<style lang="scss">
  .card {
    display: flex;
    flex-direction: column;
    border: 1px solid red;
    width: 300px;
    .card-title {
      font-size: 1rem;
      margin: 10px 0px;
    }
    ul {
      margin: 0;
      padding: 0;
      display: flex;
      gap: 5px;
      li {
        color: white;
        list-style: none;
        padding: 5px 10px;
        background-color: blue;
      }
    }
  }
  .card-lower {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .card-details {
    display: flex;
    gap: 8px;
  }
  .card-user {
    img {
      width: 25px;
      border-radius: 50%;
      margin-right: 5px;
    }
  }
</style>
