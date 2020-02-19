# useModal

[![Build Status](https://travis-ci.org/shibe97/react-hooks-use-modal.svg?branch=master)](https://travis-ci.org/shibe97/react-hooks-use-modal)

This is a react hook which can open the modal easily.

## Usage

```javascript
import React, { useState, useCallback } from 'react';
import { render } from 'react-dom';
import useModal from 'react-hooks-use-modal';
import styles from './styles.module.css';

const App = () => {
  const [Modal, open, close] = useModal('root', { preventScroll: true });
  return (
    <div>
      <button onClick={open}>OPEN</button>
      <Modal>
        <div className={styles.modal}>
          <h1>Title</h1>
          <p>This is a customizable modal.</p>
          <button onClick={close}>CLOSE</button>
        </div>
      </Modal>
    </div>
  );
};
render(<App />, document.getElementById('root'));
```

## Syntax

### [ModalComponent, openFunc, closeFunc] = useModal(domNode?, { preventScroll? })

`ModalComponent`
Modal component that displays children in the screen center.

`openFunc`
A function to open modal.

`closeFunc`
A function to close modal.

`domNode`
Optional.
Default value is 'root'.
Modal component uses React-Portal.
You can specify the output destination domNode with this argument

`preventScroll`
Optional to prevent scrolling while modal is open.
Default value is false.

## Demo

https://shibe97.github.io/react-hooks-use-modal/

## How To Develop

### Setup

```
$ npm install
```

### Build

```
$ npm run build
```

### Example

```
$ npm start
```

http://localhost:3001

## License

MIT
