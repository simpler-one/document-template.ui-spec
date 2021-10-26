# FriendList
## Image
![Image](/ui/friends/image.png)


## User can (Overview)
- look the list of friend
  - filter (optional description)
  - sort (optional description)
- jump to friend detail page
- call a friend
- ...


## URL to this page
- [ ] `/ui/friends?`
  - [ ] status: friend status to filter
  - [ ] name: friend name to filter
  - [ ] ...


## UI objects
### Header
- [ ] HamburgerMenu: XxxMenu
- [ ] Avatar: Image

### FilterForm
- [ ] Status: Pulldown
  - [ ] Online
  - [ ] Offline
- [ ] Name: Textbox
  - [ ] maxLength: 20
- [ ] ...
- [ ] ExecuteButton: Button

### FriendList
#### Header
- [ ] Check: Label
  - [ ] sortable: false
- [ ] Avatar: Label
  - [ ] sortable: false
- [ ] Buttons: Label
  - [ ] sortable: false
- [ ] *(same as body): Label
#### Body
- [ ] Check: Checkbox
- [ ] StatusIcon: Icon
- [ ] Avatar: Image
- [ ] UserName: Label
- [ ] Birthday: Label
  - format: "MM-DD"
- [ ] ...
- [ ] CallButton: Icon
  - enabled: status = Online
- [ ] MenuButton: Button


## Events
### Non user event
###### OnInit
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
- etc expectation
  - [ ] UserList sorting: UserName, Ascending

### Header
##### HamburgerMenu
###### click
- [ ] show `SideMenu`

##### Avatar
###### click
- [ ] show `AccountPopup`

###### hover
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
- FriendDetailPage
