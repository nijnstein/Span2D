<img width="416" alt="Knipsel" src="https://user-images.githubusercontent.com/96932314/188491793-e6500f9d-e52f-46b1-ad19-b34b9912da96.PNG">

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
