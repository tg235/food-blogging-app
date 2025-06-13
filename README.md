# 🍽️ Food Blogging API

A Ruby on Rails 7 (API-only) backend for a food blogging platform. 
This app provides RESTful JSON APIs to manage users, blog posts (recipes),
comments, likes, followers, and password recovery. Tested using Postman, built with scalable backend practices.

## 📦 Requirements
To run this API locally, ensure the following tools are installed:

**Ruby**: 3.0.0  
  You can use: [RVM](https://rvm.io/) or [rbenv](https://github.com/rbenv/rbenv) to manage versions

**Rails**: 7.0.7.2  
  gem install rails -v 7.0.7.2

**Bundler**
gem install bundler

**SQLite3 (for local development)**
Ubuntu: sudo apt install sqlite3 libsqlite3-dev
Windows: https://www.sqlite.org/download.html
---

## 🔧 Tech Stack

- **Ruby**: 3.0.0
- **Rails**: 7.0.7
- **Database**: SQLite 3
- **Authentication**: JWT
- **Background Jobs**: Sidekiq
- **Other Libraries**: bcrypt, rack-cors, RSpec, Faker, Will Paginate

---

## 📌 Key Features

- ✅ **JWT-based Login & Signup**
- 📝 **Create, Read, Update, Delete** Recipes (Posts)
- 💬 **Comment System** with update/delete
- ❤️ **Like / Dislike Recipes**
- 🔁 **Follow / Unfollow Users**
- 🔒 **Password Reset via Email Flow**
- 📊 **User Profiles & Followers Lists**
- 🧪 **API Tested with Postman**
- 🧵 **Sidekiq Integration** for background jobs (UI: `/sidekiq`)

---

## 📂 API Endpoints (Sample)

- `POST /user/login` → Login with credentials (returns JWT token)
- `POST /users` → Register new user
- `GET /users_profile` → View logged-in user's profile
- `POST /users/:id/follow` → Follow user
- `POST /users/:id/unfollow` → Unfollow user
- `GET /recipes` → List all recipes
- `POST /recipes` → Create new recipe
- `POST /likes/create/:id` → Like a recipe
- `DELETE /likes/dislike/:id` → Dislike/unlike
- `POST /comments/create/:id` → Add comment
- `PUT /comments/update/:id/:comment_id` → Edit comment
- `POST /password/forgot` → Request password reset
- `POST /password/reset` → Reset password

---

## 🛠️ Local Setup Instructions

### 1. Clone the repository

git clone https://github.com/tg235/food-blogging-app.git
cd food-blogging-app

# Install gems
bundle install

# Set up database
rails db:create
rails db:migrate
rails db:seed # optional

# Run the server
rails s

To run and test the APIs: 
API runs on http://localhost:3000

## Authentication (JWT)
Upon successful login, the API returns a JWT token.
Include the token in request headers for all secured endpoints-> Authorization: Bearer <your_token>


🧠 What I Learned doing this project: 
-> Designing and structuring secure, scalable APIs with Rails 7
-> Implementing token-based authentication with JWT
-> Managing user relationships (followers/following)
-> Using Sidekiq for background processing
-> Writing clean, modular code and organizing routes effectively

🔮 Future Enhancements
-> Add Swagger API docs (or Postman public docs)
-> Deploy via Render or Railway
-> Add pagination using Kaminari
-> Image upload via Active Storage or Cloudinary
-> Role-based access control (Admin/Author)

Any suggestions or collaboration are most welcome.



