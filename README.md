# Laravel API

A small CMS for portfolio projects, built during my full-stack course. An authenticated admin area manages posts, and a public JSON API exposes them to a separate front end.

Built on Laravel 9 (PHP 8), with Laravel Breeze for authentication and Sanctum installed.

## Data model

- `Post`: title, content, slug and a cover image
- `Type`: each post belongs to one type
- `Technology`: each post has many technologies (pivot table `post_technology`)

## Routes

| Where | Route | Purpose |
| --- | --- | --- |
| API | `GET /api/posts` | List posts |
| API | `GET /api/posts/{slug}` | Single post |
| Admin (login required) | `/admin` | Dashboard |
| Admin (login required) | `/admin/posts` | Post CRUD |

## Run

```bash
composer install
cp .env.example .env
php artisan key:generate
# set your database in .env, then:
php artisan migrate
php artisan storage:link
npm install && npm run dev
php artisan serve
```

## Status

Course project. Part of my portfolio: [https://andreacassini.com/projects/laravel-api](https://andreacassini.com/projects/laravel-api)
