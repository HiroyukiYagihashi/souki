## ☁️ souki(想起)
souki is a state management library for React apps.

## Getting stated
### Installing

Install souki by npm.
```shell script
npm i souki
```

### Example

```javascript
function App() {
  const InitialState = {
    count: 0
  };

  return (
    <div className="App">
      <header className="App-header">
        <SoukiProvider initialState={InitialState}>
          <SampleComponent />
        </SoukiProvider>
      </header>
    </div>
  );
}
```

```javascript
function SampleComponent() {
  const state = useSouki();
  const setSoukiState = useSetSouki();

  return (
    <>
      <p>
        {state.count}
      </p>
      <button onClick={() => {setSoukiState((s) => ({count: s.count + 1}))}}>
        up count
      </button>
    </>
  );
}
```

See the examples/create-react-app file for details.


## Contributing
Please read CONTRIBUTING.md for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning
We use [SemVer](https://semver.org) for versioning. For the versions available, see the tags on this repository.

## Authors
- [Hiroyuki Yagihashi](https://github.com/HiroyukiYagihashi)

See also the list of contributors who participated in this project.

## License
This project is licensed under the MIT License - see the LICENSE file for details
