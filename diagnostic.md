# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    Ember application router maps a URL to a route.
    An Ember route loads the template and the model.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember generate route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first one is a nested route. URL for this route will have the format
    /products/:product_id.
    The object passed to the second argument in the product route, contains the
    actual path used to reach the 'product' route.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    params.movie_id ?? not sure
    so, params.123????
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Ember application router maps a URL to a route.
    An Ember route loads the template and the model.
    When the model loads, the model hook will return the ember data record,
    which is then rendered to the template??
    ```
