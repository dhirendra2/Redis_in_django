How to use Redis with Django. Cache data with Django to load pages faster with improved performance.  I have Created one Django project to get things more familiar to you. What is Redis? - Redis is an in-memory data structure project implementing a distributed, in-memory key-value database with optional durability.  





Cache settings - 

CACHE_TTL = 60 * 1500      # cache with a time-to-live (TTL) of 25 hours

CACHES = {
    "default": {
        "BACKEND": "django_redis.cache.RedisCache",
        "LOCATION": "redis://127.0.0.1:6379/1",
        "OPTIONS": {
            "CLIENT_CLASS": "django_redis.client.DefaultClient"
        },
        "KEY_PREFIX": "example"
    }
}


