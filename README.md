# Citizen Browser - Capitol Riot on Facebook
This repository contains code to reproduce the findings featured in our story: "[Biden and Trump Voters Were Exposed to Radically Different Coverage of the Capitol Riot on Facebook](https://themarkup.org/citizen-browser/2021/01/14/biden-and-trump-voters-were-exposed-to-radically-different-coverage-of-the-capitol-riot-on-facebook)" from our series [Citizen Browser](https://themarkup.org/series/citizen-browser/).

Our methodology is described in "[How We Built a Facebook Inspector](https://themarkup.org/citizen-browser/2021/01/05/how-we-built-a-facebook-inspector)."

## Data files

`data/citizen-browser-capitol-riots-BIDEN.csv`
This CSV file contains the unique links shown to Citizen Browser panelists who reported voting for Joseph Biden in the 2020 U.S. general election, along with a count of the number of panelists who were shown the link.

`data/citizen-browser-capitol-riots-TRUMP.csv`
This CSV file contains the unique links shown to Citizen Browser panelists who reported voting for Donald Trump in the 2020 U.S. general election, along with a count of the number of panelists who were shown the link.

`data/citizen-browser-capitol-riots-OVERLAP.csv`
This CSV file contains the links that appeared in both the Biden and Trump datasets. 

## Query parameters

### Time Frame
We sought to capture the coverage of the events just before, during, and after the storming of the U.S. Capitol by supporters of President Donald Trump on Jan. 6, 2021.

Our query requested data observed between **Jan. 5, 2021**, and **Jan. 8, 2021**.

### Demographics
We filtered the data to only include observations from Citizen Browser panelists who reported voting for Joseph Biden or Donald Trump in the 2020 U.S. general election.

### Keywords
We performed a keyword search for the following terms: 
`"capitol","riot","protest","mob","rally","capitol hill","dc protests"`

We looked for these terms in Facebook posts, link URLs, and the poster's account name and page address.

### Exclusions
We excluded any posts flagged as sponsored, any posts that were clearly advertisements, and any links that were not associated with the activity surrounding the riot. 

We excluded any posts made by Facebook itself.

We excluded links from any domain that had only one link served in our dataset. 


### Data dictionary:
This applies to `data/citizen-browser-capitol-riots-BIDEN.csv` and `data/citizen-browser-capitol-riots-TRUMP.csv`.

<table border="0" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>Column</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>timestamp_EST</strong></td>
      <td>The date the post was observed in Eastern Standard Time. Format: `YYYY-MM-DD HH:MM:SS`</td>
    </tr>
    <tr>
      <td><strong>n_users</strong></td>
      <td>The number of unique panelists who saw this link.</td>
    </tr>
    <tr>
      <td><strong>url_domain</strong></td>
      <td>The domain of the link.</td>
    </tr>
    <tr>
      <td><strong>url</strong></td>
      <td>The URL of the link.</td>
    </tr>
    <tr>
      <td><strong>description</strong></td>
      <td>The text accompanying the link in the post.</td>
    </tr>
  </tbody>
</table>

---

This applies to `data/citizen-browser-capitol-riots-OVERLAP.csv`.
<table border="0" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>Column</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>url_domain</strong></td>
      <td>The domain of the link.</td>
    </tr>
    <tr>
      <td><strong>url</strong></td>
      <td>The URL of the link.</td>
    </tr>
    <tr>
      <td><strong>description</strong></td>
      <td>The text accompanying the link in the post.</td>
    </tr>
  </tbody>
</table>


## Licensing
Copyright 2021, The Markup News Inc.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.