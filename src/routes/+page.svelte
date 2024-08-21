<script>
    import "../app.css";
  
    let greeting = "";
  
    // @ts-ignore
    function onSubmit(event) {
      const name = event.target.name.value;
      // @ts-ignore
      hello.greet(name).then((response) => {
        greeting = response;
      });
      return false;
    }
  </script>
  
  <main>
    <img src="logo2.svg" alt="DFINITY logo" />
    <br />
    <br />
    <form action="#" on:submit|preventDefault={onSubmit}>
      <label for="name">Enter your name: &nbsp;</label>
      <input id="name" alt="Name" type="text" />
      <button type="submit">Click Me!</button>
    </form>
    <section id="greeting">{greeting}</section>
  </main>
  