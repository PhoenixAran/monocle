# Monocle
Basic resolution scaler module for Love2D.
I use this in my project [LoveOracle](https://github.com/PhoenixAran/LoveOracle)  
## How to use
~~~lua
local Monocle = require 'monocle'
local monocle = nil

function love.load()
  monocle = Monocle.new()
  monocle:setup({
    windowWidth = 160, 
    windowHeight = 144,
    virtualWidth = 1280,
    virtualHeight = 720,
    maxScale = 6
  }, {
    minwidth = 800,
    minheight = 600,
    vsync = true,
    resizable = true
  })
end

function love.draw()
  monocle:begin()
  ... draw stuff here
  monocle:finish()
end

function love.resize(x, y)
  monocle:resize(x, y)
end
~~~