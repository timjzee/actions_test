# actions_test

Test repo for GitHub Actions. Pull request should be made by adding/removing/adjusting the `.csv` files in `/projects`.

If a pull request is merged 2 consecutive workflows are activated:
- `.github/workflows/update-table.yml` merges `csv` files into `table.html` which is pushed to /site
- `.github/workflows/static.yml` builds and deploys the GitHub pages website, available at <timzee.nl/actions_test>

The `/site` folder contains all files for the website.
- `index.html` can be adjusted with text/info/links​. Do not remove the code that includes the table. 
- `table.html` is automatically generated after a merge​. This file is not meant to be edited manually.
- `styles.css`​ is a placeholder for css code that is applied to index.html

The following html classes are available for css:
`<th>`:
- main-header
- second-header
- row-b, only the cell containing `(maker, bases, URL)`

`<td>`:
- row-a
  - name-cell
  - data-cell
    - open, partial, closed
- row-b