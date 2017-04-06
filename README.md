# thrift-mocker

# Easy to mock data based on thrift, no hard code data anymore!

You will not need to wirte mock-data any more, All data generate automatically by this mocker.  


## Usage
```js
const thriftMocker = new ThriftMocker({
  service: "@path/to/your/file.thrift",
  models: [require("@path/to/your/model.thrift"), require("@path/to/your/another-model.thrift")],   // more than one model thrift file.
  mockData: {
    // if you really want to mock some specify method, go here! like the following:
    getSomeDataMethod: {
      // your data...
    }
  },
  commonData: {
    // some common data struct
    code: 200,
    message: "success"
  },
  cache: true,  // if not cache, will generate different data at each time. Your choice.
  serviceName: "YourSeviceName" // If your thrift service has more than one service, you have to indicate the service you need!
});
```

## Generator
In most application, your data have vast type of data, such as: img, url, text, number, price, percent, person name, goods name, etc.
In such cases, you may want to make your data more reality ( even I don't think it's necessary ), you could change the generator by youself.    
I promise I will provide a better way, maybe like a AI, to generate more reality data. Of course, in the future!