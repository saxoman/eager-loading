Optimize Laravel Eloquent Queries with Eager Loading
https://laravel-news.com/eloquent-eager-loading

php artisan tinker

>>> $posts = App\Post::with('author')->get();
>>> $posts->map(function ($post) {
...     return $post->author;
... });
...

Nested Eager Loading in Eloquent

php artisan tinker

>>> $posts = App\Post::with('author')->get();
>>> $posts->map(function ($post) {
...     return $post->author->profile;
... });
...

Lazy Eager Loading

php artisan tinker

>>> $posts = App\Post::all();
...
>>> $posts->load('author.profile');
>>> $posts->first()->author->profile;
...
