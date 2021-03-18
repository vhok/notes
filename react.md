# React Cheat Sheet
## Important React Files
**README.md**: Project documentation for repo.  
**node_modules/**: All installed node packages.  
**package.json**: List of node package dependencies & other config.  
**package-lock.json**: Node package versions breakdown.  
**.gitignore**: Files ignored during commit.  
**public/**: Development files.  


## Main Commands
- Scripts are run by npm run <script>.
- Scripts names are defined in package.json.
- *run* can be omitted for **start** and **test** commands.
  
Creates react application
```
npx create-react-app <app name>
```

Runs development server in http://localhost:3000
```
npm start
```
Run the tests
```
npm test
```
Build the application for production
```
npm run build
```
## Props
src/App.js
```javascript
const App = () => {
  const computers = ["Mac", "Asus", "Razer", "Dell", "Lenovo"];
  
  
  return (
    <div>
      <List items={computers} />  
    </div>
  );
}
```

src/List.js
```javascript
const List = (props) => {

  return (
    <p>{props.items[0]}</p>
  );
}
```

## State



## Notes
