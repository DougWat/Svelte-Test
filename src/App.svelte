<script>
  export let name;
  let count = 0;

  function handleClick() {
    count += 1;
  }
</script>

<style type="text/scss">
  $PADDING: 30px;
  .cool-card{
    padding: $PADDING;
    max-width:300px;
    background-color: rgba(230,230,240,1);
    border-radius: 10px;
    .title{
      text-align: center;
    }
    button{
      border:none;
      padding:10px 20px;
      border-radius: 5px;
      &:hover{
        background-color: gray;
        color: white;
        cursor: pointer;
      }
      transition: color 200ms, background-color 200ms;
    }
  }
</style>

<div class="cool-card">
  <h2 class="title">This is a card :)</h2>
  <hr/>
  <p>
    This is a bit of text that might appear in the card. Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores, officiis. Aspernatur error fugit ullam aut dolorum mollitia similique, consequatur quos ad explicabo voluptatibus facere possimus! Ducimus esse dolore soluta impedit?
  </p>
  <button on:click={handleClick}>I'm a button :^) Ya clicked me {count} {count === 1 ? 'time' : 'times'}</button>
</div>
