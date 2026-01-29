## 🔒 Git Workflow Policy

### Branch Strategy
- **`dev`**: Development branch - ALL team members work here
- **`staging`**: Testing/QA branch - Only Sara (QA) can merge to this branch
- **`main`**: Production branch - Controlled releases only

### Team Member Restrictions

#### All Team Members (Global Rules)
- ✅ Work on `dev` branch only
- ❌ NEVER commit directly to `staging` or `main`
- ✅ Create pull requests for review

#### Leo (Senior Developer)
- ✅ Work exclusively on `dev` branch
- ✅ Create commits with clear, descriptive messages
- ✅ Create pull requests from `dev` to `staging` after completing work
- ✅ Notify Sara for review
- ❌ NEVER merge to `staging` or `main` himself

#### Sara (QA Engineer)
- ✅ **ONLY** team member authorized to merge PRs from `dev` to `staging`
- ✅ Ensure all tests pass before merging
- ✅ Verify code quality standards are met
- ✅ Verify deployment after merge
- ✅ Document releases

#### Alex (Solutions Architect)
- ✅ If creating proof-of-concept code, work on `dev` branch only

## 📋 Workflow Summary
1. **Development**: All code changes happen on `dev`
2. **Pull Request**: Leo creates PR from `dev` → `staging`
3. **Review**: Sara reviews, tests, and approves
4. **Merge**: Sara merges to `staging` (ONLY Sara can do this)
5. **Verification**: Sara verifies staging deployment
6. **Production**: Controlled release to `main` (separate process)

This ensures proper separation of concerns and maintains code quality through our QA gate.
