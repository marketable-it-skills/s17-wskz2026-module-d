# Test Project Outline – Module D – Interactive Frontend using an API

## Competition time

3 hours

## Introduction

In this module, you must develop the client-side application (SPA) for an online classifieds service. This is a web interface that interacts with the REST API implemented in Module C.

Your task is to build a responsive frontend that supports authentication, advert management, browsing published listings, and purchasing paid promotion services through the provided API.

## General Description of Project and Tasks

The application must support working with the API: authentication, advert management, viewing specific adverts, and features related to roles and statuses.

You are provided with an **OpenAPI** specification that the API follows at [`assets/media-files/swagger/openapi.yaml`](assets/media-files/swagger/openapi.yaml). A Postman collection for API testing is available at [`assets/media-files/collection.json`](assets/media-files/collection.json). Please use the **ready-made Module C solution** when developing this module.

The API is available at: `https://module-c-api.YYYYYY.wsk.com`, where YYYYYY is your unique **subdomain**.

The following website-wide requirements apply:

- Use the provided framework from the `templates` tab in GIT
- The interface must be responsive: it must display correctly on different devices
- Implement navigation between pages (for example, using client-side routing)
- Provide error handling: invalid data, access denied, server errors, and so on
- Ensure a good user experience: data loading, spinners, notifications, action confirmations

## Requirements

The following features must be implemented.

### Authentication and Profile

- User registration. Registration form with fields: email, phone, password. Validation must be on the client side; all fields are required. After successful registration, the user is automatically logged in.
- Authentication. Sign in with email or phone + password. After login, the user receives a token that is stored on the client. The token is sent in the `Authorization` header with every request.
- Profile editing. The user can change their email, phone number, and password with validation (old, new, and repeat fields). Apply the appropriate validation rules.
- Logout. The user must be able to sign out. When they do, the token is removed from the browser.

### Adverts

Users can create adverts. The create-advert form must include: title, text, price, category, image upload.

After creation, an advert has the status `draft`. The user can submit it for moderation (status `moderation`).

Users can edit adverts. Editing is only possible in the `draft` status. The edit form is the same as the create form.

The user can also change an advert to the `archived` status.

Users can delete adverts. Deletion is only available to the author in the `draft` or `archived` status.

Users can view their own adverts. The `My Adverts` page must contain a list of the user's adverts. Adverts can be filtered by status.

### Home Page

The page displays a list of adverts. The page does not require authentication.

Display all published adverts. For each advert, show: title, short description, price, category, date.

Allow filtering adverts by selected category, price, and keywords. Price can be filtered from a minimum to a maximum value; both fields are optional.

### Advert Details Page

Users can view advert details. Display: title, description, price, category, images, publication date, author name.

Images must be displayed as a carousel: one image centered, with all other images below it. Follow standard carousel requirements.

Users can view the seller's phone number. `Show phone` button. When clicked, the phone number appears. Until then, it is hidden. While hidden, only the first 4 digits of the number are shown; the rest is hidden behind the button.

Next to the advert, display a button for purchasing paid services, as well as a list of services already purchased, together with their expiration dates.

### Purchase Page For Advantage Services

Paid services can be purchased for each advert: **VIP** (7 days) and **TOP** (3 days).

Design a unique interface for purchasing paid services, and take the modularity of this system into account.

If a service has not been purchased, the user can buy the VIP service for 7 days or the TOP service for 3 days.

If a service has already been purchased, the user can extend it after the period expires.

## Assessment

Module D will be assessed using the latest stable version of Google Chrome and Firefox. Frontend behaviour is verified against the project requirements and the provided **OpenAPI** specification. API integration is tested against the **Module C** backend using the provided Postman collection. Responsive layout, client-side routing, error handling, and user feedback (loading states, notifications, confirmations) are reviewed during evaluation.

## Mark distribution

The table below outlines how marks are broken down and how they align with the WorldSkills Occupation Standards (WSOS). Please read the Technical Description for a full explanation of the WorldSkills Occupation Standards.

| WSOS SECTION | Description                            | Points |
| ------------ | -------------------------------------- | ------ |
| 1            | Work organization and management       | 1      |
| 2            | Communication and interpersonal skills | 0      |
| 3            | Design implementation                  | 4.75   |
| 4            | Front-end development                  | 17.25  |
| 5            | Back-end development                   | 0      |
| **Total**    |                                        | **23** |
