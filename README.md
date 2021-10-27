# Quanti s.r.o. Java entry test
## A Comment Service
### General info
Your task is to implement a simple Spring Boot cz.quanti.java.entry.test.service.

1. We have prepared a base project for you, which is available in this repository. Clone it to a local repository.
2. In your local git repository, create a separate feature branch for your implementation. Commit all your code exclusively to that branch. Name your branch `feature/your-first-and-last-name`, e.g. `feature/john-doe`.
3. Implement the cz.quanti.java.entry.test.service per our requirements. You will read more about them in the following section.
4. When you are done, push the branch to our repository and create a Merge Request from your branch to `master`. Assign the merge request to ==xxx xxx== (==xxx@quanti.cz==), and email us.
5. You will get a code review from one of our developers. You *may* get several small comments on your Merge Request and be asked to improve it — don't be alarmed, that is a part of the task. We won't ask for any drastic changes.

The task is intended to take a couple of hours of your time, but that may vary depending on your level of experience.

### What we want you to implement
We have an application [java-entry-test-blog-api](https://github.com/QuantiCZ/java-entry-test-blog-api) which exposes information from our internal blog. It provides a basic API to read the details of our blog. However, currently users have no way to comment on blog posts, which is a feature that we would like.

**Your task is therefore to implement a simple comment module.** It should expose a JSON REST-like API, which should provide basic CRUD functionality:
1. Create a new comments on a blog post
2. Read all comments for a blog post
3. Update an existing comment
4. Delete an existing comment

A comment should contain the following data:
- Comment's text (`String`), *required*
- Blog post ID (`Long`), *required*
- Comment author's name (`String`), *required*
- Comment author's email (`String`), *optional*
- Creation timestamp (choose a suitable data type), *required*
- Last update timestamp (choose a suitable data type), *required*

There are three large requirements:
1. **Write your service in Java 11 (or higher) with Spring Boot**. We have predefined the libraries we think you may want to use, but you are free to add and/or change them. (note for example that we haven't provided any libraries for working with databases — that is on you!)
2. **Connect to our blog API**. You will find the application in the `blog-api` repository [java-entry-test-blog-api](https://github.com/QuantiCZ/blog-api-java-entry-test). The API is already implemented, you only need to boot it up locally. To learn how to do that, take a look at [java-entry-test-blog-api](https://github.com/QuantiCZ/blog-api-java-entry-test). Use the API to get information about the blog posts.
3. **Use an external database in a Docker container**. You should also use ORM in your application. You may use any database you like — relational (e.g., PostgreSQL, MariaDB), non-relational (e.g., MongoDB), etc.

Other than that, you are not restricted in any way! You may use any libraries you like, and change or rewrite the template we have predefined for you in any way you see fit.
