# clinicalTrialsByIntervention.rq
**Code examples:** [curl](#curl)
### SPARQL
```sparql
SELECT ?intervention ?interventionLabel (COUNT(?trial) AS ?trials) WHERE {
  VALUES ?topic {
    wd:Q84263196 wd:Q82069695
  }
  ?trial wdt:P31 wd:Q30612 ;
         wdt:P921  ?topic ;
         wdt:P4844 ?intervention .
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en,en". }
} GROUP BY ?intervention ?interventionLabel
  ORDER BY DESC(?trials)
```
[run](https://query.wikidata.org/embed.html#SELECT%20%3Fintervention%20%3FinterventionLabel%20%28COUNT%28%3Ftrial%29%20AS%20%3Ftrials%29%20WHERE%20%7B%0A%20%20VALUES%20%3Ftopic%20%7B%0A%20%20%20%20wd%3AQ84263196%20wd%3AQ82069695%0A%20%20%7D%0A%20%20%3Ftrial%20wdt%3AP31%20wd%3AQ30612%20%3B%0A%20%20%20%20%20%20%20%20%20wdt%3AP921%20%20%3Ftopic%20%3B%0A%20%20%20%20%20%20%20%20%20wdt%3AP4844%20%3Fintervention%20.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%2Cen%22.%20%7D%0A%7D%20GROUP%20BY%20%3Fintervention%20%3FinterventionLabel%0A%20%20ORDER%20BY%20DESC%28%3Ftrials%29%0A) or [edit](https://query.wikidata.org/#SELECT%20%3Fintervention%20%3FinterventionLabel%20%28COUNT%28%3Ftrial%29%20AS%20%3Ftrials%29%20WHERE%20%7B%0A%20%20VALUES%20%3Ftopic%20%7B%0A%20%20%20%20wd%3AQ84263196%20wd%3AQ82069695%0A%20%20%7D%0A%20%20%3Ftrial%20wdt%3AP31%20wd%3AQ30612%20%3B%0A%20%20%20%20%20%20%20%20%20wdt%3AP921%20%20%3Ftopic%20%3B%0A%20%20%20%20%20%20%20%20%20wdt%3AP4844%20%3Fintervention%20.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%2Cen%22.%20%7D%0A%7D%20GROUP%20BY%20%3Fintervention%20%3FinterventionLabel%0A%20%20ORDER%20BY%20DESC%28%3Ftrials%29%0A)


### Output
<table>
  <tr>
    <td><b>intervention</b></td>
    <td><b>trials</b></td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q421094">hydroxychloroquine</a> (<a href="http://www.wikidata.org/entity/Q421094">edit</a>)</td>
    <td>41</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q422438">chloroquine</a> (<a href="http://www.wikidata.org/entity/Q422438">edit</a>)</td>
    <td>14</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q422585">lopinavir</a> (<a href="http://www.wikidata.org/entity/Q422585">edit</a>)</td>
    <td>13</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q422618">ritonavir</a> (<a href="http://www.wikidata.org/entity/Q422618">edit</a>)</td>
    <td>13</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q56363387">Chloroquine diphosphate bearing dextran nanoparticles augmented drug delivery and overwhelmed drug resistance in Plasmodium falciparum parasites</a> (<a href="http://www.wikidata.org/entity/Q56363387">edit</a>)</td>
    <td>12</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q84263196">COVID-19</a> (<a href="http://www.wikidata.org/entity/Q84263196">edit</a>)</td>
    <td>11</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q425154">tocilizumab</a> (<a href="http://www.wikidata.org/entity/Q425154">edit</a>)</td>
    <td>5</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q410074">losartan</a> (<a href="http://www.wikidata.org/entity/Q410074">edit</a>)</td>
    <td>4</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q40207875">antiviral agent</a> (<a href="http://www.wikidata.org/entity/Q40207875">edit</a>)</td>
    <td>4</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q57055">acetaminophen</a> (<a href="http://www.wikidata.org/entity/Q57055">edit</a>)</td>
    <td>4</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q207843">nitric oxide (radical)</a> (<a href="http://www.wikidata.org/entity/Q207843">edit</a>)</td>
    <td>4</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q417222">methylprednisolone</a> (<a href="http://www.wikidata.org/entity/Q417222">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q11426176">prednisolone</a> (<a href="http://www.wikidata.org/entity/Q11426176">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27107351">methylprednisolone acetate</a> (<a href="http://www.wikidata.org/entity/Q27107351">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27108063">prednisolone acetate</a> (<a href="http://www.wikidata.org/entity/Q27108063">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27262132">methylprednisolone hemisuccinate</a> (<a href="http://www.wikidata.org/entity/Q27262132">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27266327">prednisolone 21-phosphate</a> (<a href="http://www.wikidata.org/entity/Q27266327">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27278862">prednisolone hemisuccinate</a> (<a href="http://www.wikidata.org/entity/Q27278862">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q3960572">Siltuximab</a> (<a href="http://www.wikidata.org/entity/Q3960572">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q188269">interferon</a> (<a href="http://www.wikidata.org/entity/Q188269">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q288280">ACE inhibitor</a> (<a href="http://www.wikidata.org/entity/Q288280">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q193598">DL-ascorbic acid</a> (<a href="http://www.wikidata.org/entity/Q193598">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q165399">azithromycin</a> (<a href="http://www.wikidata.org/entity/Q165399">edit</a>)</td>
    <td>3</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q21057316">coal tar pitch volatiles</a> (<a href="http://www.wikidata.org/entity/Q21057316">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q408524">cyclophosphamide</a> (<a href="http://www.wikidata.org/entity/Q408524">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27106392">dexamethasone acetate</a> (<a href="http://www.wikidata.org/entity/Q27106392">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q798309">BCG vaccine</a> (<a href="http://www.wikidata.org/entity/Q798309">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q3950557">Sargramostim</a> (<a href="http://www.wikidata.org/entity/Q3950557">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q9268800">gloriosine</a> (<a href="http://www.wikidata.org/entity/Q9268800">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q17149812">Janus kinase inhibitor</a> (<a href="http://www.wikidata.org/entity/Q17149812">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q415411">anakinra</a> (<a href="http://www.wikidata.org/entity/Q415411">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q155954">tenofovir</a> (<a href="http://www.wikidata.org/entity/Q155954">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q422604">emtricitabine</a> (<a href="http://www.wikidata.org/entity/Q422604">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q7383611">ruxolitinib</a> (<a href="http://www.wikidata.org/entity/Q7383611">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q7041828">nivolumab</a> (<a href="http://www.wikidata.org/entity/Q7041828">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q87775025">mRNA-1273</a> (<a href="http://www.wikidata.org/entity/Q87775025">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q413299">bevacizumab</a> (<a href="http://www.wikidata.org/entity/Q413299">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q422212">budesonide</a> (<a href="http://www.wikidata.org/entity/Q422212">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q203174">thalidomide</a> (<a href="http://www.wikidata.org/entity/Q203174">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q28209496">remdesivir</a> (<a href="http://www.wikidata.org/entity/Q28209496">edit</a>)</td>
    <td>2</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q1215575">naproxen</a> (<a href="http://www.wikidata.org/entity/Q1215575">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q249619">immunosuppressive drug</a> (<a href="http://www.wikidata.org/entity/Q249619">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q188724">non-steroidal anti-inflammatory drug</a> (<a href="http://www.wikidata.org/entity/Q188724">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q5515384">gabexate</a> (<a href="http://www.wikidata.org/entity/Q5515384">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q20817234">thymalfasin</a> (<a href="http://www.wikidata.org/entity/Q20817234">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q50840582">Angiotensin II</a> (<a href="http://www.wikidata.org/entity/Q50840582">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q2450337">interferon beta-1a</a> (<a href="http://www.wikidata.org/entity/Q2450337">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q5119448">Ciclesonide</a> (<a href="http://www.wikidata.org/entity/Q5119448">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27161510">(5R)-24,25-Dihydroxyvitamin D</a> (<a href="http://www.wikidata.org/entity/Q27161510">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q49872458">Ergocalciferols</a> (<a href="http://www.wikidata.org/entity/Q49872458">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q419618">deferoxamine</a> (<a href="http://www.wikidata.org/entity/Q419618">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27088384">piclidenoson</a> (<a href="http://www.wikidata.org/entity/Q27088384">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q668093">atorvastatin</a> (<a href="http://www.wikidata.org/entity/Q668093">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q159683">citric acid</a> (<a href="http://www.wikidata.org/entity/Q159683">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q409728">trisodium citrate</a> (<a href="http://www.wikidata.org/entity/Q409728">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27126379">sildenafil citrate</a> (<a href="http://www.wikidata.org/entity/Q27126379">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q211509">oseltamivir</a> (<a href="http://www.wikidata.org/entity/Q211509">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q3765251">darunavir</a> (<a href="http://www.wikidata.org/entity/Q3765251">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q420360">phentolamine</a> (<a href="http://www.wikidata.org/entity/Q420360">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q3836750">lopinavir/ritonavir</a> (<a href="http://www.wikidata.org/entity/Q3836750">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88454408">Xuebijing</a> (<a href="http://www.wikidata.org/entity/Q88454408">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q417097">levamisole</a> (<a href="http://www.wikidata.org/entity/Q417097">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27132391">formoterol fumarate</a> (<a href="http://www.wikidata.org/entity/Q27132391">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q239778">bromhexine</a> (<a href="http://www.wikidata.org/entity/Q239778">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q576104">neonate</a> (<a href="http://www.wikidata.org/entity/Q576104">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q27132395">fingolimod hydrochloride</a> (<a href="http://www.wikidata.org/entity/Q27132395">edit</a>)</td>
    <td>1</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q66559285">immunoglobulin</a> (<a href="http://www.wikidata.org/entity/Q66559285">edit</a>)</td>
    <td>1</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o clinicalTrialsByIntervention.rq https://raw.githubusercontent.com/egonw/SARS-CoV-2-Queries/master/sparql/clinicalTrialsByIntervention.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@clinicalTrialsByIntervention.rq
```
This SPARQL query is available under CCZero.
