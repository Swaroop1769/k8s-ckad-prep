Multi-container pod that share same lifecycle, that means they are created together and destroyed together.

they share the same network space - they can refer to each other as local host.

And they have access to same storage volumes


## Multi Container Pod Design Patterns

1. **Co-located Containers** - run throughout the pod lifecycle - usually used when 2 containers are dependent on each other.
2. **Init Containers** - initilization steps to be performed when a pod starts before main app itself. (eg: a db application to get ready and does it's job and stops before main app starts and then the main app starts)

3. **Sidecar Container** - unlike init containers the sidecar containers - main app starts after the sidecar container starts.

Co-located and Sidecar are same??? in co-located there's no order of startup on containers. However sidecar container provides ability to specify order of startup and continue to run throughout the pod lifecycle.