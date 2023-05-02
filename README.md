# This project will create a list
# We will then check to see whether its sorted
# The last function will check search to see whether an item is on the list

items1 = [4, 6, 10, 100, 95, 68, 54]
items2 = [4, 6, 10, 54, 68, 95, 100]
# this checks to see whether the list is sorted


def is_sorted(itemslist):
    return all(itemslist[i] <= itemslist[i+1] for i in range(len(itemslist) - 1))

# this searchs for items in the list


def binary_search(item, itemlist):
    list_size = len(itemlist) - 1

    loweridx = 0
    upperidx = list_size

    while loweridx <= upperidx:
        pass
        midpoint = (loweridx + upperidx) // 2

        if itemlist[midpoint] == item:
            return midpoint

        if item > itemlist[midpoint]:
            loweridx = midpoint + 1

        else:
            upperidx = midpoint - 1

    if loweridx < upperidx:
        return None


print(binary_search(100, items1))
print(binary_search(100, items2))

print(is_sorted(items1))
print(is_sorted(items2))
