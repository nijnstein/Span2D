https://user-images.githubusercontent.com/96932314/188491731-0e6ed9be-2f8b-4e84-8c72-9401b714ce5a.mp4

# Span2D<T>

A Span working on a 2 dimensional array 

```csharp

// create a span2d from an array
Span2D<float> data2d = new float[10,10].AsSpan2D(); 

// direct access through indexer 
float f = data2d[i, j];

// row access throug a span:
Span<float> row = data2d.Row(0); 

// column access via Span2D<T>.ColumnSpan
Span<float> a = stackalloc float[10]; 
data2d.Column[0].CopyTo(a); 

float[] b = data2d.Column[1].ToArray(); 

```
