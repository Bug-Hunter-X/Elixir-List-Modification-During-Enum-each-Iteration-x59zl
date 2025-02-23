# Elixir List Modification During Enum.each

This example demonstrates a common pitfall in Elixir when attempting to modify a list while iterating over it using `Enum.each`.  The issue stems from Elixir's immutable data structures.  `List.delete` creates a *new* list, leaving the original list untouched.  This code attempts to modify the list in-place, which is not how Elixir works.

The solution highlights the correct approach, using `Enum.filter` to create a new list containing only the desired elements.