<script>
// @ts-nocheck

  import { Node, Svelvet, Minimap, Controls, Background } from 'svelvet';
</script>

<div id="fixed" class="h-screen">
<Svelvet theme="dark" snapTo=22 id="my-canvas" controls>
  <Node id="A" label="WaveDream" bgColor="blueviolet" outputs=2 connections={[['B', 0], ['B', 2], ['B', 0], ['B', 3]]}/>
  <Node id="B" inputs=3 label="Dream Sequence" bgColor="turquoise" position={{ x: 300, y: 150}}/>
  <Node id="C" inputs=3 label="test" bgColor="grey" position={{ x: 500, y: 350}} />
</Svelvet>
</div>