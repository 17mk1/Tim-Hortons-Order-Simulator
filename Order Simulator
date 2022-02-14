import urllib2
  # this loads a library you will need.  Put this line at the top of your file.

def driver():
    response = urllib2.urlopen("http://research.cs.queensu.ca/home/cords2/timOrders.txt")
    html = response.readline()  # reads one line
    data = html.decode('utf-8').split()  # splits this line into a list of "tokens"  (print it to see what you get)
    while len(data) > 0:
        print(data)
        html = response.readline()  # reads one line
        data = html.decode('utf-8').split()  # splits this line into a list of "tokens"  (print it to see what you get)

    print(html)
    return data


def addToHead(theList, value):  # adds orders -works
    newNode = {}  # empty
    newNode['data'] = value
    newNode['next'] = theList
    return newNode


def createList(pythonList):  # works
    linkedList = None  # create a new, empty list
    for i in pythonList:
        linkedList = addToHead(linkedList, i)
    return linkedList  # return the head of the new list


def deleteFromEnd(theList):  # deletes orders from -works
    ptr = theList
    if ptr['next'] == None:
        return theList
    else:
        while ptr['next']['next'] != None:
            ptr = ptr['next']
        ptr['next'] = None
        return theList


def getNewItem(contents):  # gets new item (?)
    ptr = contents
    newItem = None
    for line in ptr:
        if ptr[line][0] == 'm':
            newItem = ptr[line]
            print(newItem)
    return newItem


def addNewItem(theList, newItem):  # adds new item to list (?)
    ptr = theList
    while ptr['data'][0] != 's':  # s in submit
        while type(int(ptr['data'][7])) != type(int(newItem[7])):  # if order numbers dont match
            ptr = ptr['next']  # move down the dictionary

        ptr['data'] = ptr['data'] + newItem
    return theList


def main():
    contents = driver()
    print(contents)


main()




