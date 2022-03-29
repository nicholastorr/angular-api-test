# :zap: Angular API Project

- App using a DataService with httpClient to get a JSON Observable data stream from an API and display it using the Angular async pipe.
- App also submits a simple Contact form.
- **Note:** to open web links in a new window use: _ctrl+click on link_





## :page_facing_up: Table of contents

- [:zap: Angular API Project](#:zap-angular-api-project)
  - [:page_facing_up: Table of contents](#page_facing_up-table-of-contents)
  - [:books: General info](#books-general-info)
  - [:signal_strength: Technologies](#signal_strength-technologies)
  - [:floppy_disk: Setup](#floppy_disk-setup)
  - [:computer: Code Examples](#code-examples)
  - [:cool: Features](#features)

## :books: General info

- Routing module allows user to navigate between Home, About and Contact pages.
- API json/image data displayed: firstname, lastname, email and avatar.
- Styling is pure SCSS


## :floppy_disk: Setup

- Run `npm i` to install dependencies
- Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## :computer: Code Examples

- `data.service.ts` ES6 arrow function to return observable from API using `apiResponse` interface

```typescript
getUsers = (): Observable<apiResponse> => {
  return this.http.get<apiResponse>("https://reqres.in/api/users");
};
```

- `home.component.ts` ng init. function to get observable data for the template async pipe - note: using an ES6 arrow function here would result in nothing being displayed, due the use of 'this'

```typescript
ngOnInit () {
  this.users$ = this.data.getUsers();
};
```


## :clipboard: Status & To-Do List

- Status: Working.
- To-Do: Nothing.


## :file_folder: License

- This project is licensed under the terms of the MIT license.
