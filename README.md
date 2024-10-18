# rule-engine-ast

# Rule Engine with Abstract Syntax Tree (AST)

## Overview
This project implements a simple rule engine using Abstract Syntax Trees (AST) to represent and evaluate conditional rules. The system allows for the creation, combination, and evaluation of rules based on user attributes such as age and department.

## Design Choices
1. **AST Structure**: We use a binary tree structure to represent the AST. Each node in the tree is either an operand (representing a condition) or an operator (AND/OR).
2. **Node Class**: The `Node` class is designed to be flexible, accommodating both operands and operators in a single structure.
3. **Rule Evaluation**: The evaluation is done recursively, traversing the AST and evaluating each node based on its type (operand or operator).

## Dependencies
This project is implemented in Python and doesn't require any external libraries. It uses only built-in Python modules.

- Python 3.7+

## Build Instructions
1. Ensure you have Python 3.7 or higher installed on your system.
2. Clone this repository:
   ```
   git clone https://github.com/your-username/rule-engine-ast.git
   cd rule-engine-ast
   ```
3. No additional installation steps are required as the project uses only built-in Python modules.

## Usage Examples

### Creating a Rule
```python
def create_sample_rule():
    node1 = Node("operand", value="age > 30")
    node2 = Node("operand", value="department == 'Sales'")
    root = Node("operator", left=node1, right=node2, value="AND")
    return root

rule_ast = create_sample_rule()
```

### Evaluating a Rule
```python
user_data = {"age": 35, "department": "Sales"}
result = evaluate_rule(rule_ast, user_data)
print(result)  # Output: True
```

### Running the Script
To run the script, use the following command in your terminal:
```
python rule_engine.py
```

## Future Improvements
1. Implement a parser to convert string representations of rules into ASTs.
2. Add support for more complex conditions and additional operators.
3. Implement error handling for invalid rules or data formats.
4. Create a simple UI for rule creation and evaluation.

## Contributing
Contributions to this project are welcome. Please fork the repository and submit a pull request with your changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
