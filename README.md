# DevOps Conception Class
- Student: [Pen Sreyneat]

## Lesson 2: My CI/CD pipeline
- Project: Personal Finance Management System[Flutter app + Laravel API]
- Trigger: push to feature/register [Push to practice branch]
- Target: Laravel staging server + Android testing device.[Staging + test device]

### Pipeline design
Code -> Test -> Build -> Release -> Deploy
1. Code: [action]=commit API(api/register) | [person]=PEN SREYNET | [output]=Commit code | [manual]
2. Test: [action]=Check API(api/register) | [person]=KUN TOUCH | [output]=Test result | [auto]
3. Build: [action]=Package API+APK | [person]=Artifact (MOT PHUM) | [output]=Package APK | [auto]
4. Release: [action]=Approve version v1.0.0 | [person]=release lead (SOR VEASNA) | [output]=Approve version v1.0.0 | [manual]    
5. Deploy: [action]=stage APK | [person]=Devops | [output]=Running App | [manual]
### Controls
-On test/build failure: stop release  fix issue  return test.
-Release approval by: release lead (SOR VEASNA)
-After deployment, check: register | If it fails: stop version v1.0.1 and  rollback to version v1.0.0
Optional drawing: ![My pipeline](pipeline.jpg)