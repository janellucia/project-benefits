<template>

  <div>
  <b-card title="Survey Questions" no-body>
    <h2>Survey Questions</h2>
    <b-tabs card vertical nav-wrapper-class="w-25">
      <b-tab title="Sponsor" active>
        <p><strong>Sponsors</strong> are those who were actively involved working with directing this project (e.g. requested project, prioritized project, validated acceptance criteria).</p>
        <ol>
          <li>To what degree to believe that this was an important project worth being prioritized?</li>
          <li>How satisfied are you with the value delivered by this project?</li>
          <li>How satisfied are you with the training &amp; communication provided for impacted users  and management?</li>
          <li>How satisfied are you that the project outcomes met business objectives?</li>
          <li>How satisfied are you that the project was delivered on time?</li>
          <li>How satisfied are you with the cost and adherence to budget of this project?</li>
          <li>To what degree will this project positively impact the following benefit areas?</li>
          <li>How effective were the following areas of project management?</li>
          <li>Overall project management</li>
          <li>Solution design followed best available approach</li>
          <li>Efficiency of project work and development</li>
          <li>Understanding of needs and capture of requirements</li>
          <li>Responsiveness to changing requirements</li>
          <li>Oversight and approval process</li>
          <li>Timeliness and usefulness of communication throughout the project</li>
          <li>At an estimated cost of , to what degree will the benefits of this project exceed this cost?</li>
          <li>How satisfied are you with the following?</li>
          <li>Please describe the business value and impact of this project for you.</li>
          <li>What suggestions or feedback do you have for the project team?</li>
        </ol>
      </b-tab>
      <b-tab title="Project Team">
        <p><strong>Project Team</strong> members are those who were actively involved working with delivery of this project (e.g. Developer, Analyst etc.).</p>
        <ol>
          <li>To what degree to believe that this was an important project worth being prioritized?</li>
          <li>How satisfied are you with the value delivered by this project?</li>
          <li>How satisfied are you with the training &amp; communication provided for impacted users  and management?</li>
          <li>How satisfied are you that the project outcomes met business objectives?</li>
          <li>How satisfied are you that the project was delivered on time?</li>
          <li>How satisfied are you with the cost and adherence to budget of this project?</li>
          <li>To what degree will this project positively impact the following benefit areas?</li>
          <li>How effective were the following areas of project management?
            <ul>
              <li>Overall project management</li>
              <li>Solution design followed best available approach</li>
              <li>Efficiency of project work and development</li>
              <li>Understanding of needs and capture of requirements</li>
              <li>Responsiveness to changing requirements</li>
              <li>Oversight and approval process</li>
              <li>Timeliness and usefulness of communication throughout the project</li>
            </ul>
          </li>
          <li>At an estimated cost of, to what degree will the benefits of this project exceed this cost?</li>
          <li>How satisfied are you with the following?</li>
          <li>Please describe the business value and impact of this project for you.</li>
          <li>What suggestions or feedback do you have for the project team?</li>
        </ol>
      </b-tab>
      <b-tab title="Impacted User">
        <p><strong>Impacted Users</strong> are those who did not directly work on this project but should be able to realize the benefits (e.g. business users or leaders).</p>
        <ol>
          <li>What is the seniority of your role?</li>
          <li>To what degree to believe that this was an important project worth being prioritized?</li>
          <li>How satisfied are you with the value delivered by this project?How satisfied are you with the training &amp; communication provided for this project?</li>
          <li>To what degree will this project positively impact the following benefit areas?</li>
          <li>What suggestions or feedback do you have for the project team?</li>
        </ol>
      </b-tab>
    </b-tabs>
    <small>Note the appearance of the survey will differ from this display</small>
  </b-card>
</div>

</template>

<script>

export default {
  name: 'SurveyQuestions'
}
</script>
