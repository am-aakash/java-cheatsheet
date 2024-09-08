## The Java Cheatsheet
```
        1. Map operations
        Map<String, Integer> map = new HashMap<>();

        // Add or update a key-value pair
        map.put("key", 1);

        // Get a value (returns null if key doesn't exist)
        Integer value = map.get("key");

        // Get value or default if key doesn't exist
        int valueOrDefault = map.getOrDefault("key", 0);

        // Check if key exists
        boolean containsKey = map.containsKey("key");

        // Remove a key-value pair
        map.remove("key");

        // Iterate over map
        for (Map.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }

        // Increment value for a key, handling case where key doesn't exist
        String key = "counter";
        map.merge(key, 1, Integer::sum);
        // or
        map.put(key, map.getOrDefault(key, 0) + 1);
```

```
        2. List operations
        List<Integer> list = new ArrayList<>();

        // Add elements
        list.add(1);
        list.add(0, 2); // Add at specific index

        // Remove elements
        list.remove(Integer.valueOf(1)); // Remove by value
        list.remove(0); // Remove by index

        // Get element
        int element = list.get(0);

        // Update element
        list.set(0, 3);

        // Sort list
        Collections.sort(list);

        // Binary search (list must be sorted)
        int index = Collections.binarySearch(list, 3);
```

```
        3. Stack operations
        Stack<Integer> stack = new Stack<>();

        stack.push(1); // Add to top
        int topElement = stack.pop(); // Remove and return top element
        int peekedElement = stack.peek(); // View top element without removing
        boolean isEmpty = stack.isEmpty(); // Check if stack is empty
```

```
        4. Queue operations
        Queue<Integer> queue = new LinkedList<>();

        queue.offer(1); // Add to rear
        int frontElement = queue.poll(); // Remove and return front element
        int peekedQueueElement = queue.peek(); // View front element without removing
        boolean isQueueEmpty = queue.isEmpty(); // Check if queue is empty
```

```
        5. Deque (Double-ended queue) operations
        Deque<Integer> deque = new ArrayDeque<>();

        deque.addFirst(1); // Add to front
        deque.addLast(2); // Add to rear
        int frontDequeElement = deque.removeFirst(); // Remove and return front element
        int rearDequeElement = deque.removeLast(); // Remove and return rear element
        int peekFirst = deque.peekFirst(); // View front element without removing
        int peekLast = deque.peekLast(); // View rear element without removing
```

```
        6. PriorityQueue operations
        PriorityQueue<Integer> minHeap = new PriorityQueue<>();
        PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Collections.reverseOrder());

        minHeap.offer(3); minHeap.offer(1);
 minHeap.offer(2);
        int minElement = minHeap.poll(); // Removes and returns smallest element (1)
```

```
        7. Set operations
        Set<Integer> set = new HashSet<>();

        set.add(1);
        set.remove(1);
        boolean contains = set.contains(1);
```

```
        8. Array operations
        int[] array = new int[5];
        Arrays.fill(array, 1); // Fill array with 1s
        int[] copyArray = Arrays.copyOf(array, array.length);
        Arrays.sort(array);
        int searchIndex = Arrays.binarySearch(array, 1);
```

```
        9. StringBuilder operations
        StringBuilder sb = new StringBuilder();
        sb.append("Hello").append(" World");
        sb.insert(5, "!"); // Insert at specific index
        sb.delete(5, 6); // Delete range
        String result = sb.toString();
```

```
        10. Collections utility methods
        Collections.reverse(list);
        Collections.shuffle(list);
        int max = Collections.max(list);
        int min = Collections.min(list);
        int frequency = Collections.frequency(list, 1);
```

```
        11. 2D Array operations
        int[][] matrix = new int[3][4];  // 3 rows, 4 columns
        // or
        int[][] predefinedMatrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };
```

```
        12. Convert ArrayList to Array
        List<Integer> arrayList = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5));
        array = arrayList.toArray(new Integer[0]);
```

```
        13. Convert Array to ArrayList
        String[] stringArray = {"a", "b", "c"};
        List<String> stringList = new ArrayList<>(Arrays.asList(stringArray));
```

```
        14. Sort an array
        int[] unsortedArray = {3, 1, 4, 1, 5, 9};
        Arrays.sort(unsortedArray);
```

```
        15. Binary search in a sorted array
        int[] sortedArray = {1, 2, 3, 4, 5};
        index = Arrays.binarySearch(sortedArray, 3);
```

```
        16. Create a graph using adjacency list
        Map<Integer, List<Integer>> graph = new HashMap<>();
        // Add edge from vertex 1 to 2
        graph.putIfAbsent(1, new ArrayList<>());
        graph.get(1).add(2);
```

```
        17. Use a Deque as a stack and queue
        // Deque<Integer> deque = new ArrayDeque<>();
        deque = new ArrayDeque<>();
        deque.push(1);  // Add to front (stack operation)
        deque.offer(2); // Add to end (queue operation)
        int front = deque.pop();  // Remove from front
        int back = deque.poll();  // Remove from front
    }
}
```
