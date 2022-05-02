# GeneralPolygonClipper Cheat Sheet

## Data types
```c
enum gpc_op;            // Set operation type
struct gpc_vertex;      // Polygon vertex structure
struct gpc_vertex_list; // Vertex list structure 
struct gpc_polygon;     // Polygon set structure
struct gpc_tristrip;    // Tristrip set structure
```

## Methods
```c
void gpc_read_polygon(FILE *infile_ptr, int read_hole_flags, gpc_polygon *polygon);                                                   // reads a polygon from a file
void gpc_write_polygon(FILE *outfile_ptr, int write_hole_flags, gpc_polygon *polygon);                                                // writes a polygon to a file
void gpc_add_contour(gpc_polygon *polygon, gpc_vertex_list *contour, int hole);                                                       // TODO
void gpc_polygon_clip(gpc_op set_operation, gpc_polygon *subject_polygon, gpc_polygon *clip_polygon, gpc_polygon *result_polygon);    // TODO
void gpc_tristrip_clip(gpc_op set_operation, gpc_polygon *subject_polygon, gpc_polygon *clip_polygon, gpc_tristrip *result_tristrip); // TODO
void gpc_polygon_to_tristrip(gpc_polygon *polygon, gpc_tristrip *tristrip);                                                           // Converts a gpc_polygon to a gcp_tristrip
void gpc_free_polygon(gpc_polygon *polygon);                                                                                          // Frees a polygon pointer from the heap
void gpc_free_tristrip(gpc_tristrip *tristrip);                                                                                       // Frees a tristrip pointer from the heap
```
