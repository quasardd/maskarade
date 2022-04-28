# Project Title

`maskarade` is just a small collection of a few functions that mask/unmask string based on a pattern.

### Installing

Install with npm or yarn

npm:
```
npm i --save maskarade
```
yarn
```
yarn add maskarade
```

## Usage
```ts
import { mask, unmask } from 'maskarade'


const value = '12025550178';
mask('+9 (999) 999-9999', value);
// outputs: +1 (202) 555-0178


const maskedValue = '+1 (202) 555-0178';
unmask(maskedValue);
// ouputs: 12025550178


const myMonthlySalary = '1000'; // 🥲
mask(myMonthlySalary, {
  prefix: '$',
  decimalSeparator: '.',
  groupSeparator: ',',
  precision: 2
})
// outputs: $1.000,00
```
If you need more options, check [react-native-mask-text](https://github.com/akinncar/react-native-mask-text) for reference. What is passed through props, can be passed to mask function also.

## Masks
Pattern used in masked components:

- `9` - accept digit.
- `A` - accept alpha.
- `S` - accept alphanumeric.

## Running the tests

>TODO: Implement tests

### And coding style tests

>TODO: Define this

## Contributing

Feel free to submit a PR.

## Authors

* **[Caio Henrique](https://github.com/Coystark)**
* **[Marcel P Goes](https://github.com/glothos)**

See also the list of [contributors](https://github.com/quasardd/mascarade.js/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
~~Extracted~~ Strictly copied from https://github.com/akinncar/react-native-mask-text utils. Since they have react native as specific use case, we extracted the mask logic to work in any `js/ts` environment without the need of react-native as a peer dependency.
