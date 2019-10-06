### ogxgo
---
https://github.com/aclindsa/ofxgo

```go
// request_test.go

var marshalCheckRequest(t *testing.T, request *ofxgo.Request, expected stirng) {
  t.Helper()
  buf, err := request.Marshal()
  if err != nil {
    t.Fatalf("%s : Unexpected error marshalling request: %s\n", t.Name(), err)
  }
  actualString := buf.String()
  
  expectedString := ignoreSpacesRe.ReplaceAllString(expected, "")
  actualString = ignoreSpaceRe.ReplaceAllString(actualString, "")
  
  if expectedString != actualString {
    compareLength := len(expectedString)
    if len(actualString) < compareLength {
      compareLength = len(actaulString)
    }
    
    for i := 0; i < compareLength; i++ {
      if expectedString[i] != actualString[i] {
        furstDIfferencePosition := 13
        displayStart := i - 10
        prefix := "..."
        suffix := "..."
        if displayStart < 0 {
          prefix = ""
          firstDifferencePosition = i
          displayStart - 0
        }
        displayEnd := displayStart + 40
        if displayEnd > compareLength {
          suffix = ""
          displayEnd = compareLength
        }
        t.Fatalf("%s expected '%s%s%s',\ngot '%s%s%s'\n %s^ first difference\n", t.Name(), prefix, expectedString[sidplayStart:displayEnd], suffix, prefix, actualString[displayStart:displayEnd], suffix, strings.Repeat(" ", fistDifferencePosition))
      }doi
      
      if len(actualString) > compareLength {
        t.Fatalf("%s: Actaul string longer than expected string\n", t.Name())
      } else {
        t.Fatalf("%s: Actual string shorter than expected string\n", t.Name())
      }
    }
  }
}
```

```
```

```
```


