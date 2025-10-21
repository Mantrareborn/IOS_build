# iOS POC - GitHub Actions with Fastlane

This is a minimal Proof of Concept demonstrating iOS app building using GitHub Actions and Fastlane.

## What this POC demonstrates:

1. **GitHub Actions Workflow**: Automated iOS app building on macOS runners
2. **Fastlane Integration**: Using Fastlane to build iOS apps in CI/CD
3. **Artifact Generation**: Creating and uploading IPA files as build artifacts

## Project Structure:

```
IOS_build/
├── .github/workflows/main.yml    # GitHub Actions workflow
├── fastlane/Fastfile            # Fastlane configuration
├── ios/                         # Simple iOS project
│   └── SimpleApp.xcodeproj      # Xcode project
├── Gemfile                      # Ruby dependencies
└── README.md                    # This file
```

## How it works:

1. **Trigger**: Workflow runs on push to main branch or manual dispatch
2. **Environment**: Uses macOS runner with Ruby 3.2
3. **Build Process**: 
   - Installs Fastlane via Bundler
   - Builds iOS app using Fastlane
   - Creates IPA artifact
   - Uploads artifact for download

## Key Features:

- ✅ **No Code Signing**: Simplified for POC (uses development export)
- ✅ **No Environment Complexity**: Single build configuration
- ✅ **Minimal Dependencies**: Only Fastlane and basic iOS project
- ✅ **Artifact Output**: Generates downloadable IPA file

## Usage:

1. Push code to trigger workflow
2. Check Actions tab in GitHub
3. Download IPA artifact from completed workflow

This POC proves that GitHub Actions can successfully build iOS applications using Fastlane, providing a foundation for migrating from Azure DevOps.
