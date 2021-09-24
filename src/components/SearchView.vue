<template>
    <form>
        <input type="text" placeholder="Поиск по файлам.">
        <button type="submit"></button>
    </form>
</template>

<style scoped lang="scss">
* {box-sizing: border-box;}
form {
  position: relative;
  max-width: 500px;
  margin: 0 auto;
  background: white;
  border: 1px solid #cecece;
  border-radius: 5px;
}
input, button {
  border: none;
  outline: none;
  background: transparent;
}
input {
  width: 100%;
  height: 42px;
  padding-left: 15px;
  outline: none;
  position: relative;

}

form:focus-within {
    max-width: 700px;
    transition: .3s linear;
}

button {
  height: 42px;
  width: 42px;
  position: absolute;
  top: 0;
  right: 0;
  cursor: pointer;
}
button:before {
  content: "\f002";
  font-family: FontAwesome;
  font-size: 16px;
  color: orangered;
}
</style>