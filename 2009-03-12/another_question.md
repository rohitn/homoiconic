I have a question about organizing projects:
===

If someone wrote code like this:

    class Account
      ...
    end
    
    class Customer
      ...
    end

    class Displayamajig
    
      def display_account(account)
        ...
      end
      
      def display_customer(customer)
        ...
      end
      
      ...
      
    end
    
    class Persistamajig
    
      def persist_account(account)
        ...
      end
      
      def retrieve_account(account_identifier)
        ...
      end
    
      def persist_customer(customer)
        ...
      end
      
      def retrieve_customer(customer_identifier)
        ...
      end
      
      ...
      
    end
    
    ...

Would you suggest they rewrite things like this?

    class Account
    
      def display
        ...
      end
      
      def persist
        ...
      end
      
      def retrieve(identifier)
        ...
      end
      
      ...
      
    end
    
    class Customer
    
      def display
        ...
      end
      
      def persist
        ...
      end
      
      def retrieve(identifier)
        ...
      end
      
      ...
      
    end

If so, wouldn't it make sense that if you saw an application organized like this:

[![A Standard Rails App](http://farm4.static.flickr.com/3609/3349332232_75c370f812_o.png)](http://www.flickr.com/photos/raganwald/3349332232/ "A Standard Rails App") 

That you should refactor it into this:

[![A Refactored Rails App](http://farm4.static.flickr.com/3440/3348520567_3030b63a31_o.png)](http://www.flickr.com/photos/raganwald/3348520567/ "A Refactored Rails App")

**Why? Why not??**

*Join the discussion on [Hacker News](http://news.ycombinator.com/item?id=513472)*.

---

Recent work:

* [Kestrels, Quirky Birds, and Hopeless Egocentricity](http://leanpub.com/combinators) and my [other books](http://leanpub.com/u/raganwald).
* [Cafe au Life](http://recursiveuniver.se), a CoffeeScript implementation of Bill Gosper's HashLife written in the [Williams Style](https://github.com/raganwald/homoiconic/blob/master/2011/11/COMEFROM.md).
* [Katy](http://github.com/raganwald/Katy), a library for writing fluent CoffeeScript and JavaScript using combinators.
* [YouAreDaChef](http://github.com/raganwald/YouAreDaChef), a library for writing method combinations for CoffeeScript and JavaScript projects.

---

[Reg Braithwaite](http://braythwayt.com) | [@raganwald](http://twitter.com/raganwald)