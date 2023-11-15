Certainly! Here's a concise README file for the branch on customizing behavior with composition:

```markdown
# Customizing Behavior With Composition

## Overview

This branch showcases the flexibility of composition in customizing the behavior of objects at runtime, without the need for extensive changes or new class creations.

## Scenario

In this example, the manager's payment method is changed from a fixed salary to an hourly wage during the execution of the program.

## Changes Made

- Introduced the capability to customize an employee's payroll policy at runtime.
- Demonstrated how to modify the behavior of the manager by switching to an HourlyPolicy.

## Usage

Ensure Python is installed, then run:

```bash
python program.py
```

## Modifying Payroll Policy at Runtime

You can customize an employee's payroll policy during program execution. For example, changing the manager's payment to an hourly wage:

```python
from hr import PayrollSystem, HourlyPolicy
from productivity import ProductivitySystem
from employees import EmployeeDatabase

productivity_system = ProductivitySystem()
payroll_system = PayrollSystem()
employee_database = EmployeeDatabase()
employees = employee_database.employees

# Get the manager (assuming it's the first employee in the list)
manager = employees[0]

# Customize the manager's payroll policy to hourly
manager.payroll = HourlyPolicy(55)

# Continue with the standard program flow
productivity_system.track(employees, 40)
payroll_system.calculate_payroll(employees)
```

