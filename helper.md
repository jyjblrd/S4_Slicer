## Where dijkstra is used:

fn update_tet_attributes()
---
_, paths_to_bottom = nx.multi_source_dijkstra(cell_neighbour_graph, set(bottom_cells))


fn calculate_path_length_to_base_gradient()
---
distances_to_bottom, paths_to_bottom = nx.multi_source_dijkstra(cell_neighbour_graph, set(bottom_cells))# set([x[0] for x in tet.field_data["bottom_cell_groups"]]))


Both use networkx.multi_source_dijkstra()

To Implement -> Equivalent multi_source_astar() function

Multi-source Dijkstra
---
multi_source_dijkstra(G, sources, target=None, cutoff=None, weight='weight')
[source]

Find shortest weighted paths and lengths from a given set of source nodes.

Uses Dijkstra’s algorithm to compute the shortest paths and lengths between one of the source nodes and the given target, or all other reachable nodes if not specified, for a weighted graph.

Parameters:

    GNetworkX graph
    sourcesnon-empty set of nodes

        Starting nodes for paths. If this is just a set containing a single node, then all paths computed by this function will start from that node. If there are two or more nodes in the set, the computed paths may begin from any one of the start nodes.
    targetnode label, optional

        Ending node for path
    cutoffinteger or float, optional

        Length (sum of edge weights) at which the search is stopped. If cutoff is provided, only return paths with summed weight <= cutoff.
    weightstring or function

        If this is a string, then edge weights will be accessed via the edge attribute with this key (that is, the weight of the edge joining u to v will be G.edges[u, v][weight]). If no such edge attribute exists, the weight of the edge is assumed to be one.

        If this is a function, the weight of an edge is the value returned by the function. The function must accept exactly three positional arguments: the two endpoints of an edge and the dictionary of edge attributes for that edge. The function must return a number or None to indicate a hidden edge.

Returns:

    distance, path
    pair of dictionaries, or numeric and list

        If target is None, returns a tuple of two dictionaries keyed by node. The first dictionary stores distance from one of the source nodes. The second stores the path from one of the sources to that node. If target is not None, returns a tuple of (distance, path) where distance is the distance from source to target and path is a list representing the path from source to target.

Raises:

    ValueError

        If sources is empty.
    NodeNotFound

        If any of sources is not in G.


