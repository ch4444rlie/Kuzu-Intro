# Kùzu Graph Database for Employee Information

This project demonstrates how to use [Kùzu](https://kuzudb.com/) to create a graph database using employee information in a small company, visualized with [yFiles](https://www.yworks.com/products/yfiles). It was developed to teach Kùzu graph database basics and to illustrate how graph databases can reveal connections in employee data (e.g., departments, roles, and turnover likelihood) that are less obvious in traditional tabular formats.

## Project Overview

The project builds a graph database from a dataset of employee information, including:
- **Employee ID**: Unique identifier for each employee.
- **Department**: The department they work in (e.g., HR, IT, Media).
- **Role**: Their position (e.g., Intern, Junior, Senior, Manager).
- **Color**: A scale indicating turnover likelihood (Green: unlikely, Yellow: neutral, Orange: likely, Red: very likely).

The pipeline creates a Kùzu database, defines a schema for nodes (Employee, Department, Role, Color) and relationships (WORKS_IN, HAS_ROLE, LEAVING_COLOR), populates it with data, and visualizes the connections using yFiles. The process is described as building a "skeleton" (schema), adding "flesh" (data), and inspecting the "big picture" (visualization).

## Features

- **Data Input**: Uses a Pandas DataFrame with employee data (ID, department, role, turnover color).
- **Graph Database**: Creates a Kùzu schema with nodes for Employees, Departments, Roles, and Colors, connected by relationships.
- **Relationship Mapping**: Links employees to their department, role, and turnover likelihood.
- **Visualization**: Renders an interactive graph with yFiles, using distinct colors and shapes for each node type (e.g., Employees as blue ellipses, Departments as green rectangles).
- **Learning Focus**: Demonstrates Kùzu basics (schema creation, data loading, querying) and graph visualization.

## Previous Work

This project builds on lessons from a webpages graph database (https://github.com/ch4444rlie/WebpagesGraphDatabase) project, applying:
- **Simplified Data Model**: Uses a structured employee dataset instead of scraped webpage content, focusing on clear relationships.
- **Streamlined Schema**: Defines a concise set of nodes and relationships tailored to the employee use case.
