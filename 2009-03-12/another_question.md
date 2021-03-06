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
	
Subscribe to [new posts and daily links](http://feeds.feedburner.com/raganwald "raganwald's rss feed"): <a href="http://feeds.feedburner.com/raganwald"><img src="http://feeds.feedburner.com/~fc/raganwald?bg=&amp;fg=&amp;anim=" height="26" width="88" style="border:0" alt="" align="top"/></a>

Reg Braithwaite: [Home Page](http://reginald.braythwayt.com), [CV](http://reginald.braythwayt.com/RegBraithwaiteGH0909_en_US.pdf ""), [Twitter](http://twitter.com/raganwald)