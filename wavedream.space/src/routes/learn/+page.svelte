<script>
// @ts-nocheck

import { request, gql } from 'graphql-request'

let pageKey = "EDC"

const query = gql`
query content_waveWiki_wikipage($id: ID!) {
  values: waveWiki(where: {id: $id}) {
    wikipage(pageKey: "${pageKey}")
  }
}
`;


let body = "";
let title = "";


const loadWikiPage = async () =>  {
  const { values } = await request('https://api-us-west-2.hygraph.com/v2/clh6twltz7d7301t8f4ntej96/master', query,
  {
    id: 'clh6v2clsfi880bljiqou8xa2'
  });
  body = values.wikipage.source;
  title = values.wikipage.title;
  console.log(values);
};
loadWikiPage();
</script>

<div class="flex h-screen justify-center">
  <div class="justify-center card w-96 h-96 bg-neutral shadow-xl">
    <div class="card-body">
      <h2 class="card-title">{title}</h2>
      <p>{body}</p>
    </div>
  </div>
</div>