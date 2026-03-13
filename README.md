# Priority-queue-using-List-
Data structure practical program 
# Priority Queue using List (Higher number → higher priority)

queue = []

def enqueue():
    element = int(input("Enter element: "))
    priority = int(input("Enter priority (higher number = higher priority): "))
    queue.append((element, priority))
    # Sort queue by priority (descending order)
    queue.sort(key=lambda x: x[1], reverse=True)
    print("Element added")

def dequeue():
    if not queue:
        print("Queue is empty")
    else:
        element = queue.pop(0)
        print("Removed element:", element[0], "with priority:", element[1])

def display():
    if not queue:
        print("Queue is empty")
    else:
        print("Queue elements (Element, Priority):")
        for elem in queue:
            print(elem)

while True:
    print("\n1.Enqueue 2.Dequeue 3.Display 4.Exit")
    ch = int(input("Enter choice: "))

    if ch == 1:
        enqueue()
    elif ch == 2:
        dequeue()
    elif ch == 3:
        display()
    elif ch == 4:
        break
    else:
        print("Invalid choice")
 output:
    1.Enqueue 2.Dequeue 3.Display 4.Exit
Enter choice: 1
Enter element: 101
Enter priority (higher number = higher priority): 2
Element added

Enter choice: 1
Enter element: 102
Enter priority (higher number = higher priority): 5
Element added

Enter choice: 3
Queue elements (Element, Priority):
(102, 5)
(101, 2)

Enter choice: 2
Removed element: 102 with priority: 5
