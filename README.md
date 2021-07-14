- Go function can return multiple values.
- 

Go 'If' statement
=================

- Go's if statements are like its for loops; the expression need not be surrounded by parentheses ( ) but the braces { } are required
- Variables declared by the statement are only in scope until the end of the if.

	func pow(x, n, lim float64) float64 {
		if v := math.Pow(x, n); v < lim {
			return v
		}
		return lim
	}

- Variables declared inside an if short statement are also available inside any of the else blocks

Switch in Go
============

- Switch without a condition is the same as switch true. This construct can be a clean way to write long if-then-else chains
	func main() {
		t := time.Now()
		switch {
		case t.Hour() < 12:
			fmt.Println("Good morning!")
		case t.Hour() < 17:
			fmt.Println("Good afternoon.")
		default:
			fmt.Println("Good evening.")
		}
	}


Defer in Go
===========
- A defer statement defers the execution of a function until the surrounding function returns. The deferred call's arguments are evaluated immediately, but the function call is not executed until the surrounding function returns.

	func main() {
		defer fmt.Println("world")

		fmt.Println("hello")
	}
	
Returns "hellp" "world"
