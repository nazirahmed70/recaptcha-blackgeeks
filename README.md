# RecaptchaBlackgeeks

This is just very simple Angular 5 component that implements Image-Text Recaptcha.

### HTML View
![Image of BlackGeeks-Recaptcha]
(https://i.imgur.com/o4clLc6.png)

Installation
--------------------------------------

Install it from npm:

```bash
npm install recaptcha-blackgeeks --save
```


## Usage

### Module

```typescript
...
import { BlackgeeksRecaptchaModule } from 'recaptcha-blackgeeks';
...
```

```typescript
 ...
@NgModule({
  imports: [...,BlackgeeksRecaptchaModule]
  })
  ...
```

### View

Use in template like below

```html
 <blackgeeks-recaptcha></blackgeeks-recaptcha>
```


## Methods

To access the methods, use [@ViewChild](https://angular.io/docs/ts/latest/api/core/index/ViewChild-decorator.html).

### Import
```typescript
import { ViewChild } from '@angular/core';
import { RecaptchaComponent } from 'recaptcha-blackgeeks';

export class RegisterComponent {
  @ViewChild(RecaptchaComponent) captcha: RecaptchaComponent;
}
```


### Usage
You can request a new captcha to be displayed:
```typescript
this.captcha.reset();
```

The previous response can be retrieved:
```typescript
let status = this.captcha.getResponse();
```
