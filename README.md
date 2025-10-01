# Cursor Rules Documentation

This directory contains Cursor AI assistant rules that define development standards, patterns, and best practices for Flask projects. These rules help ensure consistent code quality and architectural decisions throughout the development process.

## Overview

The rules are organized into modular strategy files (`.mdc` format) that cover different aspects of the application development lifecycle. Each rule file contains specific guidelines that the AI assistant follows when helping with code generation, refactoring, and problem-solving.

## Rule Files

### Core Architecture & Structure

#### `project_structure_strategy.mdc` 
**Always Applied**: ✅
- Defines the Flask application structure using Blueprints architecture
- Core technology stack: Python, Flask, PostgreSQL, Databricks SDK, SQLAlchemy, Alembic
- Service layer pattern implementation
- Separation of concerns between routes, services, models, and utilities

#### `configuration_strategy.mdc`
**Always Applied**: ✅
- Environment variable management using `python-dotenv`
- Configuration classes for different environments (development, production)
- Required environment variables for Flask, database, and Databricks connections

### Database & Data Management

#### `database_strategy.mdc`
**Always Applied**: ✅
- PostgreSQL connection management and pooling
- Alembic migration best practices
- SQLAlchemy model definitions using declarative base
- Timestamp handling recommendations (Unix time preference)

#### `databricks_strategy.mdc`
**Always Applied**: ✅
- Databricks SDK authentication patterns
- Environment variable requirements for Databricks integration
- Best practices for API response caching and retry logic
- Logging requirements for Databricks API calls

### Frontend & User Interface

#### `frontend_strategy.mdc`
**Always Applied**: ✅
- Milligram CSS framework integration
- Databricks brand color palette and styling guidelines
- Typography and accessibility standards
- Vanilla JavaScript patterns with modern ES6+ features
- Component interaction examples

### Development Standards

#### `style_strategy.mdc`
**Always Applied**: ✅
- Python code style enforcement (PEP 8, Black, isort, flake8)
- Naming conventions for different code elements
- Logging configuration and requirements
- Type hint usage guidelines

#### `performance_strategy.mdc`
**Always Applied**: ✅
- Database optimization techniques (indexing, pagination, eager loading)
- Caching strategies for expensive operations
- Databricks metadata caching recommendations

### Error Management & Quality Assurance

#### `error_fix_strategy.mdc`
**Always Applied**: ❌ (Context-dependent)
- Root cause analysis approach for debugging
- Flask error handler patterns for HTTP and API responses
- Databricks API error handling with user-friendly messages

#### `devops_strategy.mdc`
**Always Applied**: ❌ (Context-dependent)
- Testing framework setup with pytest
- Code coverage targets and testing patterns
- Security best practices (CSRF protection, input validation)
- Production deployment checklist

### Documentation Standards

#### `documentation_strategy.mdc`
**Always Applied**: ✅
- README.md maintenance guidelines
- Code comment and docstring standards (Google/NumPy style)
- API documentation requirements

## Rule Application

### Always Applied Rules
These rules are automatically enforced in all development contexts:
- `configuration_strategy.mdc`
- `database_strategy.mdc`
- `databricks_strategy.mdc`
- `frontend_strategy.mdc`
- `project_structure_strategy.mdc`
- `style_strategy.mdc`
- `performance_strategy.mdc`
- `documentation_strategy.mdc`

### Context-Dependent Rules
These rules are applied when relevant to the specific development task:
- `error_fix_strategy.mdc` - Applied during debugging and error resolution
- `devops_strategy.mdc` - Applied during testing, security, and deployment tasks

## Usage

The Cursor AI assistant automatically references these rules when:
- Generating new code
- Refactoring existing code
- Debugging issues
- Providing architectural guidance
- Suggesting best practices

## Customization

To modify the development standards:
1. Edit the relevant `.mdc` file
2. Update the `alwaysApply` flag if needed
3. Ensure consistency across related rule files
4. Update this README if adding new rules or changing the structure

## File Format

Each rule file follows this structure:
```markdown
---
alwaysApply: true|false
---

## Section Title
- Rule or guideline
- Code examples
```

The frontmatter determines whether the rule is always applied or only in specific contexts.
