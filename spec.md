# PageName

## URL to this page
`/url/to/page`


## Image
![Image](/ui/image.png)


## User can (Overview)
- look the list of users.
- ...


## UI objects
### HeaderArea
- HamburgerMenu
- Avatar

### MainArea
- UserList
  - Avatar
  - UserName
  - Email
  - RoleType
  - MenuButton

...


## Events
### Non user event
#### OnInit
- [ ] repuest `GetMe`
  - [ ] (OK) show `HeaderArea/Avatar`
  - [ ] (Err) show error dialog. break
- [ ] request `GetUsers`(foo=abc, bar=42)
  - [ ] (OK) show result on `UserList`
  - [ ] (Err) show error dialog. break

### HeaderArea
- HamburgerMenu
  - click
    - [ ] show `SideMenu`
- Avatar
  - click
    - [ ] show `AccountPopup`
  - hover
    - [ ] show user name

...


## Dependencies
### API
- [GetMe](link/to/get-me/spec)
- [GetUsers](link/to/get-users/spec)

### Permission
- Camera

### Page
- HogePage
