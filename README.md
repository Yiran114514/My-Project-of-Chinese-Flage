import turtle

# 设置画布
screen = turtle.Screen()
screen.title("中国国旗")
screen.setup(width=600, height=400)
screen.bgcolor("red")

# 创建画笔
pen = turtle.Turtle()
pen.speed(3)

# 绘制大五角星
def draw_star(x, y, size):
    pen.penup()
    pen.goto(x, y)
    pen.pendown()
    pen.color("yellow")
    pen.begin_fill()
    for _ in range(5):
        pen.forward(size)
        pen.right(144)
    pen.end_fill()

# 绘制大星星
draw_star(-250, 150, 50)

# 绘制小五角星
small_stars_positions = [(-200, 180), (-170, 150), (-170, 110), (-200, 80)]
for pos in small_stars_positions:
    draw_star(pos[0], pos[1], 20)

# 隐藏画笔
pen.hideturtle()

# 保持窗口打开
turtle.done()
