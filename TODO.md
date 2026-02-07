# TODO

- [ ] Ajouter un PAT pour inclure les stats des repos privés
  1. Créer un Fine-grained token sur https://github.com/settings/tokens?type=beta
     - Name : `profile-summary`
     - Expiration : 1 an
     - Repository access : All repositories
     - Permissions : `Contents: Read-only`
  2. Ajouter le token comme secret `PAT` sur https://github.com/AlexandreHagen/AlexandreHagen/settings/secrets/actions
  3. Remplacer `GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}` par `GITHUB_TOKEN: ${{ secrets.PAT }}` dans `.github/workflows/profile-summary.yml`
