# Pharmacist inbox setup (Firebase, free Spark plan)
1. Go to console.firebase.google.com > Add project.
2. Build > Firestore Database > Create database (production mode, nearest region).
3. Rules tab: paste firestore.rules, replace ADMIN@EMAIL.COM with your email, Publish.
4. Build > Authentication > Get started > Email/Password > Enable. Users tab > Add user (your admin email + a password).
5. Project settings (gear) > General > Your apps > Web (</>) > register. Copy apiKey and projectId.
6. In index.html AND admin.html set: const FB={project:"YOUR_PROJECT_ID",key:"YOUR_API_KEY"};
7. Upload to GitHub. Users' questions now appear in admin.html > Pharmacist inbox; your replies show up in their Ask chat within ~15 seconds.
The apiKey is public by design; the rules above are what protect the data.
