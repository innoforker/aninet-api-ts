# AniNet API Typescript
Import this module to your project and use the whole functionality, including available interfaces.  
Made for aninet.gagl.art  
Originally was created for the desktop client but was abandoned

# Docs!
- Interfaces
  - Just check it yourself... There are a lot of interfaces and types.
- Functions
  - GetRelease(animeId: number, lang: "ru" | "en" = "ru") returns the info about specific release
    - Params:
      - animeId — unique ID of your release
      - lang — language of the content
    - Returns **ListAnimeResponse** or **null** if there is an error
  - GetUserProfile(userId: number) returns the info about specific user
    - Params:
      - userId — the ID of specific user on the website
    - Returns **UserProfile** or **null** if there is an error
  - ListAnime
    - *Just use ListAnimeDefault() without args and don't worry*
    - Returns **ListAnimeResponse[]** or **null** if there is no data
  - ListAnimeById(userId: number, userState: "completed" | "plantowatch" | "banned", lang: "ru" | "en" = "ru") returns specific user's bookmarks which you can filter
    - Returns **UserAnimeResponse[]** or **null** if there is no data
  - SignIn(email: string, password: string)
    - Returns response including token (**SignUpResponse**) by email and password if account exists, if not, it returns **null**
  - SignUp(name: string, password: string, email: string, genderId: 1 | 2)
    - Same as SignIn but you need to specify more args. genderId is male (1) and female (2)
