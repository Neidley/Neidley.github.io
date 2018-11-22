---
layout: page
title: About
permalink: /about/
feature-img: "img/color.png"
---

```ruby
def create
  @post = Post.new(post_params)
  project_id = 'landmarks-183414'
  image_path = @post.image.staged_path
  vision = Google::Cloud::Vision.new project: project_id
  image = vision.image image_path
  image.landmarks.each do |landmark|
    @post.name = landmark.description
        landmark.locations.each do |location|
          @post.location = "#{location.latitude},#{location.longitude}"
        end
  end
```

Everyday I code, I get to learn and create something new and feed my natural curiosity.

13 projects in the 18 months,
75+ hours pair-programming with senior developers,
open-source source contributions,
solid understanding of software engineering principles.

{:.center}
<img src="/img/bloc_certificate.png" alt="Bloc Certificate" style="width: 450px;"/>

A favorite project of mine uses **Google’s Vision API** and **Amazon Web Services**. It allows users to identify and save images of landmarks and provides a link to Wikipedia. (Landmark Discoveries) [Landmark Discoveries](https://landmark-discoveries.herokuapp.com/users/sign_up)

{:.center}
<img src="/img/landmarkdiscoveries1.png" alt="Landmark Discoveries" style="width: 450px;"/>

I’m a software engineer, specializing in full-stack web applications. I have a passion for all things development, with a keen interest in JavaScript and Ruby, and expertise in various frameworks including Rails, React, Node.js, PostgreSQL, and Firebase.

And I couldn't have gotten to this point without the support of my wife and our two dogs.

{:.center}
![]({{ site.baseurl }}/img/neidleys.png)

{:.center}
![]({{ site.baseurl }}/img/dogs.png)
