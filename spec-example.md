# FriendList
## Image
![Image](/ui/friends/image.png)


## User can (Overview)
- look the list of friend.
- ...


## URL to this page
- [ ] `/ui/friends?`
  - [ ] status: friend status to filter
  - [ ] name: friend name to filter
  - [ ] ...


## UI objects
### Header
- [ ] HamburgerMenu: xxx
- [ ] Avatar: Image

### FilterForm
- [ ] Status: Pulldown
  - [ ] Online
  - [ ] Offline
- [ ] Name: Textbox
  - [ ] MaxLength: 20
- [ ] ...
- [ ] ExecuteButton: Button

### FriendList
- [ ] StatusIcon: Icon
- [ ] Avatar: Image
- [ ] UserName: Label
- [ ] Email: Link
- [ ] Birthday: Label
  - Format: "MM-DD"
- [ ] MenuButton: Button


## Events
### Non user event
##### OnInit
- assain from URL params
  - [ ] FilterForm.Status: status
  - [ ] FilterForm.Name: name
  - [ ] ... 
- [ ] repuest `GetMe`
  - [ ] params: none
  - [ ] (OK) show `HeaderArea.Avatar`
  - (Err)
    - [ ] show error dialog
    - [ ] break
- [ ] request `GetFriends`
  - params
    - [ ] staus: FilterForm.Status
    - [ ] name: FilterForm.Name
    - [ ] ...
  - (OK) show result on `FriendList`
    - [ ] .Status: status
    - [ ] .Avatar: avatar_url
    - [ ] .Name: name
    - [ ] ...
  - (Err)
    - [ ] show error dialog
    - [ ] break

### Header
#### HamburgerMenu
##### click
- [ ] show `SideMenu`

#### Avatar
##### click
- [ ] show `AccountPopup`

##### hover
- [ ] show user name

### FilterForm
  

...


## Dependencies
### API
- [GetMe](link/to/get-me/spec)
- [GetFriends](link/to/get-friends/spec)

### Permission
- Camera

### Page
- HogePage
