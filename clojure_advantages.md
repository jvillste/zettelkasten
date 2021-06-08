# Clojure advantages

## Keywords are functions

	(group-by :a [{:a 1} {:a 2}])

instead of JavaScript:

	Immutable.fromJS([{a: 1}, {a: 2}]).groupBy(value => value.get('a'))
	
## Only prefix notation

	(update-in {:a 1} [:a] + 5)
	
instead of JavaScript:

	Immutable.Map({a: 1}).updateIn(['a'], value => value + 5)
	
and

	(update-in {:a {:b 1}} [:a] assoc :c 2)
	
instead of JavaScript:

	Immutable.fromJS({a: {b: 1}}).updateIn(['a'], value => value.set('c', 2))
	
