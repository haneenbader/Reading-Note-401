# Hashtable


_What is a Hashtable?_

The Hashtable class implements a hash table, which maps keys to values. Any non-null object can be used as a key or as a value. To successfully store and retrieve objects from a hashtable, the objects used as keys must implement the hashCode method and the equals method.  


_Declaration:_

public class Hashtable<K,V> extends Dictionary<K,V> implements Map<K,V>, Cloneable, Serializable

Type Parameters:

    K – the type of keys maintained by this map
    V – the type of mapped values


_Why do we use them?_

    Hold unique values
    Dictionary
    Library


_Internal Methods :_
     
     Add()
     Find()
     Contains()
     GetHash()