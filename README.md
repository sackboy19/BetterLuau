# BetterLuau
- BetterLuau is a version of Luau with better and more concise syntax, for people who are annoyed with Luau's long keyword names.
- It is a superset of Luau, meaning it still supports regular Luau syntax.
- This language isn't usable yet as I am currently working on the transpiler that I will release here in the near future.
- Example:
```luau
-- local function
var fn do_thing(x: number)
  print(x)
end

var my_table = {x = "hello world"}

-- regular function
fn my_table.display()
  print(my_table.x)
end

print("Hello")
```

# Syntax additions
### Note that these are all optional, and you can use regular Luau keywords wherever you want
1. `var` is another way to represent `local`
2. `fn` is another way to represent `function`
3. `bool` is another way to represent `boolean`
4. `int` and `float` can be used to represent `number`, this doesn't change the underlying data-type, however it provides a bit more clarity into how you expect the variable to be used.

# Other information
- I will most likely add things in the future, however things like using curly braces `{}` for scopes instead of `then` `end` is something I probably will not add, as Luau already is very table heavy, and curly braces are everywhere. I belive this change would be too annoying for a transpiler at the moment. However my opinion may change in the future.

# Transpilation back to normal Luau
One problem with using this superset, is that you can no longer run your Luau code. Therefore we need a transpiler. I am currently working on a BetterLuau -> Luau transpiler, and I will release it here. I am also working on a 
basic editor that supports BetterLuau.

# Syntax highlighting (VS Code)
- For now you can just use this extension: https://marketplace.visualstudio.com/items?itemName=UnderMyWheel.roblox-lua
- Then find the `undermywheel.roblox-lua-1.0.5` folder in your VSCode extensions folder, and replace `syntaxes/luau.tmLanguage.json` with the one found in this repository.
