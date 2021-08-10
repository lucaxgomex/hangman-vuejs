<template>
  <div id="footer-container">
    <footer id="footer">
      <h6><a href="https://www.facebook.com/profile.php?id=100057494871754">Facebook</a></h6>
      <h6><a href="https://github.com/lucaxgomex">GitHub</a></h6>
      <h6><a href="mailto: lucas.g.oliv.dev@gmail.com">Gmail</a></h6>
      <h6><a href="https://www.linkedin.com/in/lucas-gomes-7a6a091b4/#">LinkedIn</a></h6>
      <h6><a href="https://linktr.ee/lucaxthegomex">Linktree</a></h6>
      <h6><a href="https://telegram.me/lukk4z">Telegram</a></h6>
    </footer>
  </div>
</template>

<style>

#footer {
  position: fixed;
  display: flex;
  justify-content: space-around;
  bottom: 0px;
  left: 0px;
  right: 0px;
  top: auto;
  width: 100%;
  text-align: center;
  margin-bottom: 10px;
}

a {
  text-decoration: none;
}

#footer a:hover {
  transition: 0.3s;
  color: var(--color-text-title);
}
</style>
