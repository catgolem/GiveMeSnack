<template>
    <div>
        <header>
        <h1 class="title">タイトル</h1>
            <nav class="nav">
                <ul class="menu-group">
                    <li class="menu-item"><a href="#">項目1</a></li>
                    <li class="menu-item"><a href="#">項目2</a></li>
                    <li class="menu-item"><a href="#">項目3</a></li>
                    <li class="menu-item"><a href="#">項目4</a></li>
                    <li class="menu-item"><a href="#">項目5</a></li>
                </ul>
            </nav>
        </header>
    </div>
</template>

<style>
header {
  display: flex;
  width: 100%;
  height: 100px;
  background-color: darkgrey;
  align-items: center;
}
 
.title {
  margin-right: auto;
}
 
.menu-item {
  list-style: none;
  display: inline-block;
  padding: 10px;
}
</style>
