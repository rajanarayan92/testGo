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
