# Elixir-ttimff
Elixir things that I may forget forever

- Atoms are not garbage collected. That means if we create an Atom in our program, it lives forever -> Since an Atom created lives forever, it’s not a good idea to dynamically create Atoms from user input. -> A malicious user could technically max out the total number of Atoms that can be created in a system thereby bringing the system to halt.
- Lists are stored in memory as linked lists, meaning that each element in a holds its value and points to the following element until the end of the list is reached
- Tuples, on the other hand, are stored contiguously in memory. This means getting the tuple size or accessing an element by index is fast. However, updating or adding elements to tuples is expensive because it requires copying the whole tuple in memory.
- Internally, Elixir uses a List of two elements Tuple to build a Keyword List

  `iex(1)> [{:a, 1}, {:b, 2}]`

  `[a: 1, b: 2]`
- Unlike Keyword Lists, keys in a Map cannot be repeated
- Elixir consider any value that other than false or nil to be true
- and operator requires the left side operand to be true or false, while the && accept any value