# Scope
- ## [NextJS](#nextjs)
- ## [Algorithms](#algorithms)


## Nextjs

- ### Object Destructuring
	You can avoid 'prop' by using object destructuring, example:
	```
	function Header({ title })
	{
		console.log(title);
		return <h1>React</h1>
	}
	```	
	Then you render:
	```
	ReactDOM.render(<Header />, app);
	```

- ### Navigation between pages

	Using Link component in React instead of <a> makes the client navigation faster than usual browser page transition.
	
	Do not use it for external pages.

- ### Side Notes
	
	Minification is important, since it reduces the file size.

## Algorithms

- ### Pointers (and unidimensional arrays), pointers to pointers (and multidimensional arrays), and function pointers
	
	Just an approach to pointers, the interesting things for me were:
		- void pointers and how it can be used to accept any type of data;
		- when using multidimensional arrays as parameters, we need to specify the column value so the compiler makes the correct pointer arithmetic.
