# Binary Tree Interactive Visualization

Explore and manipulate a binary tree through an intuitive, web-based interface with animated node operations.

![Balanced Tree Example](/photos/balanced.png)

Inspired by the [Binary Tree Visualization Challenge](https://thecodingtrain.com/CodingChallenges/065.2-binary-tree-viz.html) from Coding Train.

## Understanding Binary Trees

A binary tree is a data structure where each node has up to two children. The left child holds a value smaller than its parent, while the right child holds a value larger than its parent.

![Binary Tree Diagram](https://www.baeldung.com/wp-content/uploads/2017/12/Tree-1.jpg)

For a deeper dive, check out [this guide](https://www.cs.cmu.edu/~adamchik/15-121/lectures/Trees/trees.html) from Carnegie Mellon University.

## How to Use the Visualization

Upon opening, the visualization displays an empty canvas.

![Empty Canvas](/photos/blank.png)

- **Add a Node**: Click the **Add** button, input an integer, and observe the animation as the node is inserted. The newly added node appears in green. Pan by clicking and dragging, or zoom by scrolling.
  
![Single Node Example](/photos/singlenode.png)

- **Add Multiple Nodes**: Repeatedly click **Add** to insert more nodes, with animations showing their placement. Blue highlights nodes visited during insertion. Adjust the **Animation Speed** slider to speed up or slow down the process.

![Multiple Nodes Example](/photos/manynodes.png)

- **Search for a Value**: Click **Search**, enter a previously added integer, and watch the tree highlight the search path. Blue indicates visited nodes, red marks branches where the value isn’t found, and green highlights the target node (if found).

![Search Example](/photos/search.png)

- **Clear the Tree**: Click **Clear** to reset the visualization to its initial empty state.

- **Fill the Tree**: Use the **Fill** button to populate the tree with a specified number of nodes, animating each insertion. This clears the existing tree.

- **Quick Fill Option**: Click **Quick Fill** to instantly populate the tree with nodes without animation, also clearing the current tree.

![Fill Example](/photos/fill.png)

## Code Organization

- **Node.js**: Defines the Node class, the core component of the binary tree, storing a value, references to left and right children, and display properties like coordinates and colors.
- **Tree.js**: Manages the Tree class, wrapping the root node and handling operations like searching and animating node insertions.
- **Controls.js**: Implements the Controls class, linking interface buttons (e.g., Clear, Quick Fill) to the Tree class’s animation functions.
- **Explorer.js**: Controls the Explorer class, enabling panning and zooming for smooth navigation across the tree.
- **sketch.js**: Initializes all components needed to run the visualization.

**Refer to each file for detailed documentation and explanations of class functionality.**

## Technologies Used

- [p5.js](https://p5js.org/): A JavaScript library for creating interactive canvas-based visualizations.

## Future Enhancements

- Implement self-balancing with [AVL tree rotations](https://www.cise.ufl.edu/~nemo/cop3530/AVL-Tree-Rotations.pdf).
- Add animations for node deletion.
- Optimize the Explorer class for better performance with large trees using SVG rendering.
