---
title: "Seefood - image recognition system"
date: 2019-05-06T01:00:36+08:00
draft: false
---
🌟  *3rd place in 23rd International ICT Innovative Services Awards* 🌟

Seafood is an innovative app that helps foodies recognize cuisine from attractive photos and assists cooks in getting recipes and ingredient details. It also enables users to easily search for recipes by on hand ingredients, thereby helping them use up the food stored in fridges.<!--more-->

The app supports voice typing, because we know that cooks’ hands are never spared in the kitchen. Additionally, the app welcomes all users to share their creative recipes, building up the community on our app and feeding our model training database simultaneously.

# **Project Prompt**
Due to the current fitness trend, more and more people want to cook for themselves at home. However, it's never easy for a beginner who wants to make a wonderful dish just by referring to a drool-worthy cuisine photo.
Therefore, we created "Seefood" app to solve this pain point. Help people see what's in their food and easily replicate it in their kitchens.

# **Main Feature**
-  **Seefood**: Upload your food image and receive the recognition result paired with recipes and ingredient used.
- **My Ingredient**: Search for recipes by on-hand ingredients. Voice typing is supported.
- **My Recipe**: Users can share their original recipes with the community
- **Food Court**: A social community on Seefood where people can browse others’ recipes and leave comments to interact with the authors.

# **My Role**
- Project Ideation
- User Research
- User Case
- User Flow
- UI/UX Design
- Wireflow

# **My Tool**
- Slack
- Figma
- HackMD

# **User Flow**
![User Flow](https://drive.google.com/uc?export=view&id=1cEfk8tzQZ3pYoA_075QbnKd_OCAg3G62)


# **User Case**

| Item | Content |
| ---  | ---     |
| Name | Seefood |
| Actor| User    |
| Goal | To recognize the image uploaded by the user |
| Preconditions | N/A |
| Postconditions| N/A |
| Main Success Scenario |1. The user take a photo or selects a photo from their album.{{< line_break >}}  2. The user uploads the photo to the Seefood system.{{< line_break >}} 3. The system displays the accurate recognition result including ingredient and recipe information and relevant results. |
| Alternative Scenario | The system may provide an incorrectly matched result, caused by{{< line_break >}}  1. Low-quality image input {{< line_break >}} 2. Problems with the dataset {{< line_break >}} |
|  | The user may not receive any result, if there are internet connectivity issues or other factors. |


| Item | Content |
| ---  | ---     |
| Name | My ingredient |
| Actor| User  |
| Goal | To search for recipes by including ingredients|
| Preconditions  | N/A |
| Postconditions | N/A |
| Main Success Scenario |1. The user input ingredients they have.{{< line_break >}} 2. The system searches for and returns relevant results with at least a 50% match in ingredients.{{< line_break >}} 3. The user can check the search results and the ingredient and recipe information. |
| Alternative Scenario | The system returns no result if the ingredient search does not match any recipe data. |
| Special Requirement | The ingredient input filed must support Google voice typing. |

| Item | Content |
| ---  | ---     |
| Name | My recipe |
| Actor| User    |
| Goal | To create a new recipe on system |
| Preconditions | The user must be signed in. |
| Postconditions | The recipe created by the user is added to the list.  |
| Main Success Scenario | 1. The user input the recipe content and ingredients.{{< line_break >}} 2. The user submit it to the system.{{< line_break >}} 3. The system successfully adds the new recipe to the list.{{< line_break >}} 4. The user can view the newly created recipe in the list. |
| Alternative Scenario | The user isn't signed in. Redirect to the sign-in page. |
|  | If the creation is unsuccessful, alert by snack bar. |

| Item | Content |
| ---  | ---     |
| Name | Food court |
| Actor | User |
| Goal | 1. To browse and search for recipes.{{< line_break >}}2. For signed-in users, to save a recipe to favorites and leave a comment. |
| Preconditions | The user must be signed in to use “save to favorite” and “comment” function. |
| Postconditions | The latest saved recipe is added to the favorite list and the latest comment is shown on the individual recipe page. |
| Main Success Scenario | 1. All users can browse and search all recipes on the system.{{< line_break >}} 2. Signed-in users can save a recipe to their favorite list, and a “Saved to favorites” snack bar pop up.{{< line_break >}} 3. Signed-in users can leave a comment on the individual recipe page. |
| Alternative Scenario | The user not signed in wants to save the recipe to favorites. Redirect to the sign-in page.|
| | The user not signed in wants to leave a comment. Redirect to the sign-in page. |
| | If saving to favorites fails. Alert by snack bar. |
| | If leaving a comment fails. Alert by snack bar. |

# **UI/UX Flow**
![UI/UX Flow](https://drive.google.com/uc?export=view&id=1wpT1ew8K8GQIcsMXGnPglj_ty1H_p8_q)

# **Demo Video**
{{< vimeo 805473526 >}}

# **UI/UX Redesign**
## Food Court - Home Page
![Home Page](https://drive.google.com/uc?export=view&id=1dhJ9TcvmFBBaVmOzGxUza_sVzgXi8HNw)
### Existing problems
- Display only a few items on one page
- Waste most of the screen space
- Scrolling direction is limited
### New solution
- Catalog recommended items (and add a dedicated item list page for the same category)
- Make the default text smaller, freeing up more space for recommended items and popular item list
- Add vertical scrolling direction for usability

## Food Court - Individual Food Page
![Individual Food Page](https://drive.google.com/uc?export=view&id=1MLZMa009sCeLLFIe1gncQDccG-9RzVZl)
### Existing problems
- Messy interface design (without grid system design)
- Unnecessary information (such as "title", "author" and "submit time")
- Lack of clear information hierarchy
- One-line comment wastes too much vertical space (Browsing more than two comments at the same time is difficult.)

### New solution
- Redesign the interface layout (implement grid system) to improve visual organization and clarity
- Remove each information title to create a intuitive and minimalist design
- Emphasize the recipe title using Header 2 size and semi-bold weight (create a typography system)
- Redesign the comment component
    - For typography, distinguish reviewer's name and content with different font size and weight
    - Set "hug content" for a single comment component height (making it adaptive based on its content)

## My ingredient - From ingredient
![From ingredient](https://drive.google.com/uc?export=view&id=12k8NrRwsmHIZLrnj8m6npQn61GYorPOW)
### Existing problems
- Users are unable to delete or add an ingredient individually (must be sequentially)
### New solution
- Add a delete button for each ingredient input to improve flexibility and allow users to delete individual items more easily (improving user experience)
- Enlarge the add button in the comfortable thumb zone
- Add frequently input tags to reduce repetitive actions for users (improving user experience)


## Seefood - Reframe the photo
![Reframe the photo](https://drive.google.com/uc?export=view&id=1UQJ4VEEMgtHzavqGRAn_EUFdWptB9wh9)
### New solution
- Reframe photos before uploading to the system to improve recognition accuracy and enhance the user experience

## Seefood - Search Result Page
![Search Result Page](https://drive.google.com/uc?export=view&id=11z_jKNvd6Q1XqFXwZl5JEfqPc2S5NXx9)
### Existing problems
- Unclear information hierarchy
- Unnecessary title (such as "Search Result")

### New solution
- Enlarge the space of the search result and attached the uploaded image (redefine information hierarchy)
- Add ingredient, recipe lookup and save to favorite function on the same page (improving user experience)
- Add a new image recognition button to the search bar to improve the user experience for users who have more than one image recognition demand
