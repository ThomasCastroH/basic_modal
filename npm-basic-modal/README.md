# NPM-SIMPLE-MODAL

[NPM-SIMPLE-MODAL](https://www.npmjs.com/package/npm-basic-modal)

## Installation

```
npm install npm-basic-modal
```

## How to use

### Basic

#### Standalone component

    ```
    import Modal from 'npm-basic-modal';

    const YourComponent = ({show, setShow}) => {
        return (
            {/* Modal display */}
            <Modal show={show} setShow={setShow} closeAnywhere={true} showIcon={true}>
                {/* Modal content */}
                <span> Modal customized text </span>
            </Modal>
        )
    }
    ```

#### Display modal in your app
    
    ```
    import YourComponent from './YourComponent';

    const App = () => {
        const [show, setShow] = useState(false);

        return (
            {/* Exemple of trigger */}
            <button onClick={() => setShow(true)}>
                Show modal
            </button>

            {/* Modal display */}
            <div>
                <YourComponent show={show} setShow={setShow} />
            </div>
        )
    }
    ```

### Props
`show`: boolean. Show or hide the modal.
`setShow`: function. Set the show state.
`closeAnywhere`: boolean. Close the modal when click outside.
`showIcon`: boolean. Show or hide the basic close icon.
`overlayClassname`: string. Customize the overlay classname.
`sectionClassname`: string. Customize the section classname.
`iconClassname`: string. Customize the icon classname.
`overlayStyle`: object. Customize the overlay with inline-style.
`sectionStyle`: object. Customize the section with inline-style.
`iconStyle`: object. Customize the icon with inline-style.