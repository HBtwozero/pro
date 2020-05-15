# lms

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).





### Potential Database Setup
### Book Shema
-isbn  
 type: String,
      required: true,
      minlength: 13,
      maxlength: 13,
title
      type: String,
      required: true,
      maxlength: 255,
author
      type: String,
      required: true,
      maxlength: 255,
numberOfCopies     
     type: Number,
      required: true,
      min: 1,
stock
    type: Number,
images

updatedBy     
type: Schema.Types.ObjectId,
      ref: 'user',
      
### Loan Shema
book
    type: Schema.Types.ObjectId,
      ref: 'book',
      required: true,
member
      type: Schema.Types.ObjectId,
      ref: 'user',
      required: true,
issueDate
      type: Date,
      required: true,
dueDate
      type: Date,
      required: true,
returnDate
 type: Date,
createdBy
  type: Schema.Types.ObjectId,
      ref: 'user',
updatedBy
    type: Schema.Types.ObjectId,
      ref: 'user',
