 
![Knipsel](https://user-images.githubusercontent.com/96932314/188491951-514119ce-8249-4bae-8b9b-80d2f9e89b24.jpg)

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
