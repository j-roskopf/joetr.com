---
title: 'Render #2'
---

```kotlin
fun main() {
    application {
        configure {
            width = 2560
            height = 1440
            windowResizable = true
        }
        program {
            extend {
                drawer.clear(ColorRGBa.PINK)
                drawer.fill = ColorRGBa.WHITE
                drawer.stroke = ColorRGBa.BLACK
                drawer.strokeWeight = 1.0

                val circles = List(50000) {
                    Circle(Math.random() * width, Math.random() * height, Math.random() * 10.0 + 10.0)
                }
                drawer.circles(circles)
            }
        }
    }
}
```