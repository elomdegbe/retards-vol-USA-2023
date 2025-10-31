<section class="card" id="project-overview">
  <h2>Analyse des causes de retard des vols US – 2023</h2>
  <p>
    Ce projet SQL analyse les retards des vols aux États-Unis en 2023 pour identifier les principales causes et déterminer les compagnies les plus affectées.
    Les données utilisées proviennent de la table <code>us_flights_2023</code>, contenant pour chaque vol le nom de la compagnie et les retards par cause : météo, compagnie, contrôle aérien (NAS), sécurité et avion précédent.
  </p>
</section>

<section class="card" id="objectives">
  <h3>Objectifs</h3>
  <p>
    L’objectif principal est de comprendre quelles causes contribuent le plus aux retards et quelles compagnies sont les plus impactées par chacune de ces causes.
  </p>
  <p>
    Les analyses incluent :
  </p>
  <ul>
    <li>Identifier le top 10 des compagnies les plus affectées par les retards météo.</li>
    <li>Calculer la répartition globale des retards par cause sur l’ensemble des vols.</li>
    <li>Produire des données agrégées pour visualisation ou reporting.</li>
  </ul>
</section>

<section class="card" id="methodology">
  <h3>Méthodologie et requêtes SQL</h3>
  <p>
    Les requêtes SQL suivent deux grandes étapes :
  </p>
  <ol>
    <li>
      <strong>Top 10 compagnies impactées par la météo :</strong>
      <p>
        Agrégation des retards par compagnie et par cause, conversion en milliers d’heures, calcul du pourcentage de chaque cause dans le retard total de la compagnie, puis tri par pourcentage de retard météo.
      </p>
    </li>
    <li>
      <strong>Répartition globale des retards par cause :</strong>
      <p>
        Agrégation des retards pour l’ensemble des vols, transformation en format long pour chaque cause, conversion en milliers d’heures et calcul des pourcentages pour identifier les causes les plus significatives.
      </p>
    </li>
  </ol>
</section>

<section class="card" id="technologies">
  <h3>Technologies et outils</h3>
  <ul>
    <li>SQL (PostgreSQL, MySQL ou autre SGBD compatible)</li>
    <li>CTE (Common Table Expressions) pour organiser les requêtes</li>
    <li>Fonctions d’agrégation : <code>SUM</code>, <code>ROUND</code></li>
    <li>Filtrage et tri : <code>ORDER BY</code>, <code>LIMIT</code></li>
  </ul>
</section>

<section class="card" id="outputs">
  <h3>Fichiers et résultats attendus</h3>
  <p>
    <strong>Top 10 compagnies impactées par la météo :</strong> retard total par cause et pourcentage de retard dû à la météo.
  </p>
  <p>
    <strong>Répartition globale des retards :</strong> pourcentage et retard total par cause pour l’ensemble des vols, prêt pour visualisation graphique.
  </p>
</section>

<section class="card" id="remarks">
  <h3>Remarques importantes</h3>
  <p>
    La qualité des résultats dépend de l’exactitude des données de la table <code>us_flights_2023</code>. 
    Les retards sont cumulés et convertis en milliers d’heures pour faciliter l’interprétation.
  </p>
  <p>
    Ce projet est destiné à un usage éducatif et analytique.
  </p>
</section>


