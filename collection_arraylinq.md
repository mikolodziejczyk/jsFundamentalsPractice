Array linq-like operations
=======

Goto:

http://localhost:8080/collection_arraylinq.html

All operation using native array.prototype methods.

1. Where: You have window.companies. Get those for which City === "Gliwice"
2. Where with index: Employing element index in where predicate: In the previous example, change the 
condition so that
City === "Gliwice" && companies[index-1].City == "Gliwice" - that is ones for which both this and previous 
element is set to the city.

3. First: Get the first element that satisfies the predicate.
In  window.companies get the first element for which 
  a) City == "Katowice"
  b) City == "Katowice!" => not found; return null in this case


4. Concat: Combining arrays into a new one, duplicates preserved.
You have
var a2 = ["Pablo","Ana","Tom","Patti"]
Create a new array that is a1 and a2.


5. Unique: From the previous point, remove the duplicates.

6. Union:  Combining arrays into a new one, duplicates removed.
Create a new array that is a1 and a2 but w/o duplicates.


6. Intersect, Except
Create a new array that is:
 a) a1 intersect a2
 b) a1 except a2

7. OrderBy: Create a new array, that contains companies ordered by by City, check whether the results are in 
the proper order, respecting locale.


8. Reverse: Reverse the order of the array from the previous point.

9: Skip and Take: from a1 (create a new collection)
 - take the first 3 elements
 - skip the first 4 elements, take rest
 - paging: skip the first 3 elements, take 2 subsequent

10. Select - from companies create a new array that 
 a) contains only a city
 b) contains objects like { id: CompanyId, name: Name1, index: theIndexInTheSourceArray }
    Show the results with the $("#result").text(JSON.stringify(r))
 c) contains arrays like [item.CompanyId,item.Name1,index]
    Show the results with the $("#result").text(JSON.stringify(r))


11. ToLookup and SelectMany
 a) from the companies create a new array that contains objects like { id: CompanyId, name: Name1, city: City 
}
 b) from the previously created objects, create a lookup where key is city.toUpperCase();
 c) flatten the values of the lookup, i.e. perform SelectMany on lookup values


12. Any and All: check whether in companies
 a) in any element item.City == "Gliwice"
 b) in all elements item.City == "Gliwice"


13. Aggregate
How do you aggregate values?
let an = [["Tom","Marry"],["Jenny","John"]]
Make it a flat array, also in the opposite direction.
