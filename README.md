| Name           | NRP        | Kelas     |
| ---            | ---        | ----------|
| Samuel Josefano Kaloh | 5025221065 | Jaringan Komputer (I) |
| Muhammad Tharq Darobi | 5025231163 | Jaringan Komputer (I) |

## Overview
A web application project for Hotel Reviews in which customers can create their own review with ratings, and comments.

**Website Demonstration:** https://youtu.be/a9dFM-vZlns

![image](https://github.com/user-attachments/assets/da0f80b9-31cf-4f94-93b3-9b6d8df43de6)

## Pages
### Homepage
In the Homepage, there are several features created:
* **Website Logo**</br>
  API which only give the first letter of the website's name
* **Search Bar**</br>
  _currently not working, only a decoration_
* **Sign In & Register Button**</br>
  This feature is differed when a user are **authenticated** and **not authenticated**
  * **Not Authenticated**</br>
    ![image](https://github.com/user-attachments/assets/0fdd4013-5f65-4a26-8f4c-acee0418f6e8)
  * **Authenticated**</br>
    ![image](https://github.com/user-attachments/assets/889323fc-c18a-49ed-a5f0-071f0264ec79)
* **Highlighted Review**</br>
  Shows several user's review</br>
  ![image](https://github.com/user-attachments/assets/f363a123-ea3b-466c-be7f-727ba0a8e749)</br>
  **Source Code**
  ```php
      <div class="review-header">
        <h1>Some Review(s) by Customers</h1>
        @foreach ($reviews as $review)
          @if ($loop->iteration == 6)
            @break
          @endif
          <div class="review-container">
            <h2>{{ $review->hotel->name }}</h2>
            <h5>Author: {{ $review->user->name }}</h5>
            <h5>Rating: {{ $review->rating }}.0/5.0</h5>
            <p>
              {{ $review->content }}
            </p>
          </div>
        @endforeach
      </div>
  ```



