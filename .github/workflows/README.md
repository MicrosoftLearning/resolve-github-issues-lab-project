# ContosoShopEasy Training Issue Creator

This GitHub Actions workflow creates training issues for the ContosoShopEasy security training course. It generates 10 comprehensive security issues that learners will use GitHub Copilot to identify and fix.

## How to Use

### For Course Instructors

1. **Students should import this repository** using GitHub Importer to create their own copy
2. **After importing**, students run this workflow to create the training issues in their repository
3. **Students then use GitHub Copilot** to identify and fix each security vulnerability

### Running the Workflow

1. Go to the **Actions** tab in your GitHub repository
2. Find the workflow named **"Create ContosoShopEasy Training Issues"**
3. Click **"Run workflow"**
4. In the confirmation field, type exactly: `CREATE`
5. Click **"Run workflow"** to start

⚠️ **Important**: You must type `CREATE` exactly as shown to confirm issue creation.

## What Issues Are Created

The workflow creates **10 security training issues** covering real-world vulnerabilities:

### Critical Priority (Fix First)
- **Hardcoded Admin Credentials** - Remove hardcoded admin username/password
- **Credit Card Data Storage** - Fix PCI DSS compliance violations

### High Priority
- **SQL Injection Vulnerability** - Secure product search functionality  
- **Weak Password Hashing** - Replace MD5 with secure hashing
- **Sensitive Data in Logs** - Remove passwords/cards from debug output
- **Input Validation Bypass** - Fix validation that detects but allows threats

### Medium Priority
- **Predictable Session Tokens** - Implement cryptographically secure tokens
- **Weak Email Validation** - Improve email format validation
- **Insufficient Password Requirements** - Strengthen password complexity rules

### Low Priority
- **Information Disclosure** - Reduce verbose error messages and debug output

## Issue Features

Each issue includes:
- **Detailed vulnerability description**
- **Code examples** showing the security problem
- **Security risk assessment** 
- **Step-by-step fix guidance**
- **Acceptance criteria** for verification
- **Appropriate labels** for organization

## Training Flow

1. **Run the workflow** to create all training issues
2. **Read the summary issue** for course overview and instructions
3. **Start with Critical priority issues** and work down by priority
4. **Use GitHub Copilot** to understand and fix each vulnerability:
   - Ask Copilot to explain the security issue
   - Request secure coding alternatives
   - Get implementation help and code suggestions
5. **Test fixes** by running the application after each change
6. **Mark issues as complete** when vulnerabilities are resolved

## GitHub Copilot Integration

This training is designed specifically for GitHub Copilot:
- Issues contain **detailed context** for better Copilot suggestions
- **Code examples** help Copilot understand the security problems
- **Acceptance criteria** guide Copilot toward secure solutions
- **Progressive difficulty** builds security knowledge systematically

## Files Modified During Training

Students will work with these files:
- `ContosoShopEasy/Security/SecurityValidator.cs`
- `ContosoShopEasy/Services/UserService.cs`
- `ContosoShopEasy/Services/PaymentService.cs`
- `ContosoShopEasy/Services/ProductService.cs`
- `ContosoShopEasy/Services/OrderService.cs`
- `ContosoShopEasy/Models/Order.cs`

## Safety Notes

- ✅ **Safe for learning** - All vulnerabilities are intentional and educational
- ❌ **Never use in production** - This code contains deliberate security flaws
- 🎯 **Real-world examples** - Vulnerabilities represent actual security issues
- 📚 **Learning focused** - Designed to teach secure coding practices

## Support

If the workflow fails to run:
1. **Check permissions** - Ensure Actions are enabled in repository settings
2. **Verify input** - Make sure you typed `CREATE` exactly
3. **Check rate limits** - GitHub API has rate limits for issue creation
4. **Try again** - Re-run the workflow if it times out

The workflow creates issues safely and will not overwrite existing content.