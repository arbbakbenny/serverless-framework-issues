Serverless Framework issue  [#7472](https://github.com/serverless/serverless/issues/7472)

Running `serverless package --stage dev --service service1` results with file `thisshouldnotendup.txt` (and everything else in the root dir) in the package when it should be excluded because of

`7472-include-yml/services/service1/service.yml`:
<pre>
package:
  include:
    - services/service1/src/**
  exclude:
    - ./**
</pre> 