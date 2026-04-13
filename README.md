# Chat-Messaging-App-Using-Kotlin-java


Project Summary 
App Name: Mas Chat 
Type: Android Real-Time Chat Application 
Language: Java (main code) + Kotlin (Gradle scripts) 
Framework: Android Studio 
Backend: Firebase (Auth, Realtime Database, Storage, FCM) 
Compile SDK: 35 
Min SDK: 26 
Target SDK: 35 
Java Compatibility: 17 
Dependencies Used 
Core Android Libraries 
• androidx.core:core-ktx → Essential Android extensions 
• androidx.appcompat:appcompat → Compatibility support 
• com.google.android.material:material → Material Design UI components 
• androidx.constraintlayout:constraintlayout → Layout system for modern UI 
• androidx.activity:activity → Manages lifecycle and UI interaction 
Firebase Libraries 
• com.google.firebase:firebase-bom:33.9.0 → Firebase Bill of Materials (manages 
all Firebase versions) 
• com.google.firebase:firebase-auth → User Authentication (Email, Password, 
Phone) 
• com.google.firebase:firebase-database → Real-time Chat Storage 
• (Also likely firebase-storage and firebase-messaging — inferred from app type) 
• com.google.gms:google-services → Links Firebase services to the app 
  Development Tools 
• viewBinding = true → Simplifies UI element access in Java code 
• proguard-rules.pro → Code optimization & obfuscation (for release build) 
 
   App Functionalities (Based on Code Files) 
Feature Description 
  User Authentication Login/Signup using Email/Password or Phone via Firebase Auth. 
   One-to-One Chat ChatDetailActivity.java handles private user messaging in real 
time. 
   Group Chat GroupChatActivity.java allows multiple users to communicate 
in a shared group. 
     Add/Find Users AddUserActivity.java lists all users from Firebase DB and 
allows selection to start chat. 
        Home Screen (Chat 
List) 
MainActivity.java shows recent chats, messages, and online 
users. 
    Settings/Profile 
Management 
Settings.java enables changing user info (e.g., name, profile 
picture). 
       Phone-based Signup Signupwithphone.java handles OTP-based registration (Firebase 
phone auth). 
     Media Sharing 
(optional) Uses Firebase Storage for sending and retrieving images. 
    Real-Time Updates Firebase Realtime Database pushes instant updates to all users 
without reloads. 
       User Status Online/offline indicators for each user (if implemented via Firebase 
presence API). 
   RecyclerView UI Displays chat messages and user lists in scrollable modern UI 
layouts. 
�
�️ Circular Profile 
Images Likely using libraries such as CircleImageView. 
        Gradle Kotlin DSL Uses new .kts syntax for cleaner Gradle management. 
 
    Highlight Features (Important Functionalities) 
1. Firebase Integration (Main Strength) 
o Provides full cloud backend: login, chat, media, and database sync. 
2. Real-Time Chat Engine 
o Uses Firebase’s real-time event listeners to update chat instantly. 
3. Phone Authentication (OTP) 
o Secure login via mobile number and verification code. 
4. Group Chat System 
o One of the advanced chat app features rarely seen in beginner projects. 
5. ViewBinding Support 
o Simplifies UI handling (avoids findViewById). 
6. Clean Modern UI 
o Material Design components with responsive layout. 
7. User Management & Profiles 
o View, add, and update user information. 
8. Firebase Cloud Storage (Inferred) 
o Handles profile pictures or media file uploads. 
9. Compatibility with Android 8+ (SDK 26–35) 
o Ensures modern API features and backward compatibility. 
10. Kotlin + Java Hybrid Setup 
• Modern build setup while keeping Java for logic (faster builds & compatibility). 
How It Works (Workflow) 
1. App Launch → Authentication Check 
o If user is logged in, open main chat screen. 
o If not, go to signup/login page. 
2. Firebase Sync 
o Fetch user list → Load all available contacts. 
o Listen for message updates in Firebase Database. 
3. Chat Communication 
o User selects a contact → Opens ChatDetailActivity. 
o Message typed → Stored in Firebase → Auto-synced on both users’ screens. 
4. Group Chat 
o Group messages are stored under a shared group node in Firebase. 
o All members receive updates in real time. 
5. Profile & Settings 
o User can update name, image, and view account details. 
o All data synced to Firebase for persistence. 
In Summary 
Mas Chat is a fully functional Firebase-based real-time Android chat app featuring: 
•    Real-time private and group chat 
•    Firebase Authentication (Email/Phone) 
•    Firebase Realtime Database 
•    Modern UI (Material + ViewBinding) 
•    Kotlin-based Gradle with Java core 
•    SDK 35 support (latest Android compatibility) 
