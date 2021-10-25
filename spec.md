# PageName

## URL to this page
- [ ] `/ui/friends?`
  - [ ] status
  - [ ] name
  - [ ] ...


## Image
![Image](/ui/friends/image.png)


## User can (Overview)
- look the list of friend.
- ...


## UI objects
### HeaderArea
- [ ] HamburgerMenu: xxx
- [ ] Avatar: Image

### MainArea
- FilterForm
  - [ ] Status: Pulldown
    - [ ] Online
    - [ ] Offline
  - [ ] Name: Textbox
    - [ ] MaxLength: 20
  - [ ] ...
  - [ ] ExecuteButton: Button
- FriendList
  - [ ] StatusIcon: Icon
  - [ ] Avatar: Image
  - [ ] UserName: Label
  - [ ] Email: Link
  - [ ] MenuButton: Button

...


## Events
### Non user event
#### OnInit
- set URL params
  - [ ] FilterForm.Status: status
  - [ ] FilterForm.Name: name
  - [ ] ... 
- [ ] repuest `GetMe`
  - [ ] params: none
  - [ ] (OK) show `HeaderArea.Avatar`
  - [ ] (Err) show error dialog. break
- [ ] request `GetFriends`
  - params
    - staus: FilterForm.Status
    - name: FilterForm.Name
  - [ ] (OK) show result on `FriendList`
    - .Status: status
    - .Avatar: avatar_url
    - .Name: name
    - ...
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

### MainArea
- FilterForm
  

...


## Dependencies
### API
- [GetMe](link/to/get-me/spec)
- [GetFriends](link/to/get-friends/spec)

### Permission
- Camera

### Page
- HogePage
