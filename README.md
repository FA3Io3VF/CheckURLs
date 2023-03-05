# CheckURLs
Javascript Check URL Snippet


```javascript

    IsURLSyntax = (url) => {
      /* RegExp reference: https://www.debuggex.com/r/KaJrYj7vm9pKgOhK */
      const strRegex = "^((https|http|ftp|rtsp|mms)?://)"
          + "?(([0-9a-z_!~*'().&=+$%-]+: )?[0-9a-z_!~*'().&=+$%-]+@)?"
          + "(([0-9]{1,3}\.){3}[0-9]{1,3}"
          + "|"
          + "([0-9a-z_!~*'()-]+\.)*"
          + "([0-9a-z][0-9a-z-]{0,61})?[0-9a-z]\."
          + "[a-z]{2,6})"
          + "(:[0-9]{1,4})?"
          + "((/?)|"
          + "(/[0-9a-z_!~*'().;?:@&=+$,%#-]+)+/?)$";
      var re=new RegExp(strRegex);
      return re.test(url);
    }
  
      isValidURL(url, protocols = ['http', 'https', 'ftp']) {
        try {
          const { protocol } = new URL(url);
          if (this.IsURLSyntax(url)) {
            return protocols.includes(protocol);
          }
          else {
            return false
          }
        } catch (_) {
          return false;
        }
      }
      
 ```
 
 ### Note: Regexp source: https://www.debuggex.com/r/KaJrYj7vm9pKgOhK
