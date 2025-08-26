---
name: refine-prompt
description: Simple and fast prompt refinement tool that transforms brief user inputs into detailed, actionable instructions. Returns the refined prompt for you to review and use, rather than executing it directly.
allowed-tools: none
argument-hint: "<brief_prompt>" (the prompt you want to refine and clarify)
---

Transform your brief prompts into clear, detailed instructions and return them for your review and use.

**IMPORTANT: This command generates and displays refined prompts for you to copy and use - it does NOT execute the prompts.**

## Command Usage

```bash
# Generate refined prompt for authentication
/refine-prompt "Add user authentication"
# → Returns detailed authentication requirements for you to copy

# Generate refined prompt for bug fixing  
/refine-prompt "Fix login issue"
# → Returns detailed debugging steps for you to copy

# Generate refined prompt for performance improvement
/refine-prompt "Improve app performance"
# → Returns detailed optimization requirements for you to copy
```

## What This Command Does

**Simple Generation Process:**
1. **Analyze** your brief input for intent and scope
2. **Expand** with specific technical details and actionable steps
3. **Clarify** requirements, constraints, and expected outcomes
4. **Display** the refined prompt for you to copy and use

**Output Format:**
```markdown
# 🔄 Refined Prompt (Ready to Copy)

[Your detailed, expanded prompt with specific requirements and actionable steps]

---
## 📋 How to Use
1. Review the refined prompt above
2. Copy it if it meets your needs
3. Paste it into a new Claude Code session
4. Modify as needed for your specific requirements
```

## Example Transformation

**Your Input:** "Add user authentication"

**Generated Output:**
```markdown
# 🔄 Refined Prompt (Ready to Copy)

Implement a comprehensive user authentication system:

Technical Requirements:
- Design secure login/logout functionality with session management
- Implement password hashing using bcrypt with proper salt rounds  
- Create JWT token-based authentication with refresh token support
- Add input validation for email/username and password requirements
- Design user registration flow with email verification
- Implement "forgot password" functionality with secure reset tokens

Implementation Steps:
- Set up authentication middleware for protected routes
- Create user model with secure password storage
- Design login/logout API endpoints with proper error handling
- Add authentication state management in frontend
- Create user registration and profile management interfaces
- Implement proper session timeout and security headers

Quality Requirements:
- Write unit tests for authentication functions
- Add integration tests for login/logout flows
- Ensure HTTPS enforcement and secure cookie settings
- Document authentication API endpoints and usage

---
## 📋 How to Use
1. Review the refined prompt above
2. Copy it if it meets your needs  
3. Paste it into a new Claude Code session
4. Modify as needed for your specific requirements
```

## Benefits

- **Fast Generation**: Lightweight, no complex logic or file reading
- **Clear Output**: Immediate, detailed prompt ready to copy and use
- **Review Before Use**: You can modify the refined prompt before using it
- **Focused Purpose**: Pure prompt refinement without execution complexity

This streamlined approach gives you detailed, actionable prompts that you can review, modify, and use when ready.