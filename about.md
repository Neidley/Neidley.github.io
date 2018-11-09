---
layout: page
title: About
permalink: /about/
feature-img: "img/color.png"
---

I left retail after 10 years to become a software developer because
I love learning, creating, and analytical thinking.
I'm so glad I did.

At the same time, I'm grateful for my past experiences; managing a team taught me
how to create action plans, identify successful behaviors, and the importance of celebrating small successes everyday.

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

I have created 13 projects in the last year and a half, pair-programmed for over 75 hours with amazing senior developers, worked on open-source projects of my own and others, and everyday I am humbled at the creative possibilities that coding provides.

{:.center}
<img src="/img/bloc_certificate.png" alt="Bloc Certificate" style="width: 450px;"/>

One of my favorite projects uses the **Google’s Vision API** and **Amazon Web Services**, called Landmark Discoveries. It allows users to identify and save images of landmarks and provides a link to Wikipedia. (Feel free to check it out!) [Landmark Discoveries](https://landmark-discoveries.herokuapp.com/users/sign_up)

{:.center}
<img src="/img/landmarkdiscoveries1.png" alt="Landmark Discoveries" style="width: 450px;"/>

I am passionate about continuing to grow into a better developer everyday.

And I couldn't have gotten to this point without the support of my wife and our two dogs.

{:.center}
![]({{ site.baseurl }}/img/neidleys.png)

{:.center}
![]({{ site.baseurl }}/img/dogs.png)

Here's <a href="https://docs.google.com/document/d/19J3BQb-YMyl6MfMpmVz8PK0FCvnjRty_CFM9NXOUEqo/edit?usp=sharing">My Resume</a> : )
