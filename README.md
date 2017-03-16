# qr-code-react
==========

This is an npm module ported from [HERE](https://github.com/cmanzana/qrcode-npm) to work for React.

This was to fix the issues involving `dangerouslySetInnerHTML`.

## Examples

``` javascript
import QRcodeReact, { qrcode } from 'qr-code-react';

// Inside a react component:
render() {
  return (
    <div className="App">
      <QRcodeReact
        className="LOL"
        value="Hello World!"
        margin={40}
        size={10}
        codeType={4}
        errorLevel="M"
        color="#000000"
        bgColor="#FFFFFF"
      />
    </div>
  );
}


// Or just use the original code:
let qr = qrcode(4, 'M');
qr.addData("Hello World!");
qr.make();

qr.createImgTag(4);    // creates an <img> tag as text
qr.createTableTag(4);  // creates a <table> tag as text
```

## Details

``` javascript
static propTypes = {
  className:  PropTypes.string.isRequired,
  margin:     PropTypes.number,
  size:       PropTypes.number,
  codeType:   PropTypes.number,
  errorLevel: PropTypes.string,
  value:      PropTypes.string.isRequired,
  color:      PropTypes.string,
  bgColor:    PropTypes.string
};

static defaultProps = {
  margin:     2,
  size:       4,
  codeType:   4,
  errorLevel: "M",
  color:      "#000000",
  bgColor:    "#FFFFFF",
};
```


## Install

  `npm install qr-code-react`


## NOTICE

  The word "QR Code" is registered trademark of DENSO WAVE INCORPORATED
