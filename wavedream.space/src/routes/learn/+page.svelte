<script>
// @ts-nocheck

import { request, gql } from 'graphql-request'

const query = gql`
query content_page_wikipage($id: ID!) {
  values: page(where: {id: $id}) {
    wikipage
  }
}
`;


let body = "";


const loadWikiPage = async () =>  {
  const { values } = await request('https://api-us-west-2.hygraph.com/v2/clh6twltz7d7301t8f4ntej96/master', query,
  {
    id: 'clh6v2clsfi880bljiqou8xa2'
  });
  body = values.wikipage.source;
  console.log(values);
};
loadWikiPage();
</script>

<div class="flex justify-center">
  <div class="justify-center card w-96 bg-neutral shadow-xl">
    <div class="card-body">
      <p>{body}</p>
    </div>
  </div>
</div>