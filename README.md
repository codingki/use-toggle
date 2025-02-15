<!-- markdownlint-disable MD033 MD036 MD041 -->

# use-toggle

![npm](https://badgen.net/npm/v/@kodingdotninja/use-toggle)
![packagephobia/install](https://badgen.net/packagephobia/install/@kodingdotninja/use-toggle)
![packagephobia/publish](https://badgen.net/packagephobia/publish/@kodingdotninja/use-toggle)

Toggle custom hook and component wrapper for React 🔦

---

**Table of contents**

- [Installing](#installing)
- [Example usage](#example-usage)
  - [Toggle hook - `useToggle()`](#toggle-hook---usetoggle)
  - [Toggle wrapper - `<ToggleWrap />`](#toggle-wrapper---togglewrap-)
- [API](#api)
  - [Toggle hook](#toggle-hook)
  - [Toggle wrapper](#toggle-wrapper)
- [Suggestions and/or questions](#suggestions-andor-questions)
- [Maintainers](#maintainers)
- [License](#license)

---

## Installing

```sh
# using npm
npm install @kodingdotninja/use-toggle

# using yarn
yarn add @kodingdotninja/use-toggle
```

## Example usage

### Toggle hook - `useToggle()`

Use it as your usual hooks. `disable`, `enable`, or `toggle` does not accept parameters so you can use it on `onClick` handlers.

```jsx
import { useToggle } from "@kodingdotninja/use-toggle";

function App() {
  const { state, disable, enable, set, toggle } = useToggle();
  return (
    <div>
      <span>State: {state ? "enabled" : "disabled"}</span>
      <button onClick={disable}>toggle</button>
      <button onClick={enable}>toggle</button>
      <button onClick={() => set(true)}>set true</button>
      <button onClick={toggle}>toggle</button>
    </div>
  );
}
```

### Toggle wrapper - `<ToggleWrap />`

Component which wraps the children with its internal hooks. Use this if you do not want to declare another component and just wrap it.

```jsx
import { ToggleWrap } from "kodingdotninja/use-toggle";

function App() {
  return (
    <ToggleWrap>
      {({ state, disable, enable, set, toggle }) => (
        <div>
          <span>State: {state ? "enabled" : "disabled"}</span>
          <button onClick={disable}>toggle</button>
          <button onClick={enable}>toggle</button>
          <button onClick={() => set(true)}>set true</button>
          <button onClick={toggle}>toggle</button>
        </div>
      )}
    </ToggleWrap>
  );
}
```

## API

### Toggle hook

TODO

### Toggle wrapper

TODO

## Suggestions and/or questions

Head over to our [dedicated Discord channel for `use-toggle`](https://discord.gg/KsHtDasn7e).

## Maintainers

- Griko Nibras ([@grikomsn](https://github.com/grikomsn))

## License

[MIT License, Copyright (c) 2021 Koding Ninja](./LICENSE)
