### Ops manager manipulations

<a href="https://github.com/pivotal-cf/om">OM CLI Reference </a>

```
version                         prints the om release version
help                            prints this usage information
bosh-env                        prints bosh environment variables

export-installation             exports the installation of the target Ops Manager
```


### Template: 
  config-template                 **EXPERIMENTAL** generates a config template from a Pivnet product

### Product manipulations

#### All products
```
available-products              list available products
staged-products                 lists staged products
deployed-products               lists deployed products
apply-changes                   triggers an install on the Ops Manager targeted
delete-unused-products          deletes unused products on the Ops Manager targeted
delete-installation             deletes all the products on the Ops Manager targeted

```

```$xslt
pending-changes                 checks for pending changes

```

#### One product
```$xslt

Product info: 
    download-product                downloads a specified product file from Pivotal Network
    upload-product                  uploads a given product to the Ops Manager targeted
    stage-product                   stages a given product in the Ops Manager targeted
    staged-manifest                 prints the staged manifest for a product
    staged-config                   generates a config from a staged product

Stemcell: 
    upload-stemcell                 uploads a given stemcell to the Ops Manager targeted
    assign-stemcell                 assigns an uploaded stemcell to a product in the targeted Ops Manager
    assign-multi-stemcell           assigns multiple uploaded stemcells to a product in the targeted Ops Manager 2.6+

cleanup/delete: 
    unstage-product                 unstages a given product from the Ops Manager targeted
    delete-product                  deletes a product from the Ops Manager

```
#### Director configurations
```$xslt
  configure-director              configures the director

```

#### Advanced information
```$xslt
  create-vm-extension             creates/updates a VM extension
```
----
  deployed-manifest               prints the deployed manifest for a product


--- All commands
```shell script

  activate-certificate-authority  activates a certificate authority on the Ops Manager
  bosh-diff                       **EXPERIMENTAL** displays BOSH manifest diff for the director and products
  certificate-authorities         lists certificates managed by Ops Manager
  certificate-authority           prints requested certificate authority
  configure-authentication        configures Ops Manager with an internal userstore and admin user account
  configure-ldap-authentication   configures Ops Manager with LDAP authentication
  configure-product               configures a staged product
  configure-saml-authentication   configures Ops Manager with SAML authentication
  create-certificate-authority    creates a certificate authority on the Ops Manager
  credential-references           list credential references for a deployed product
  credentials                     fetch credentials for a deployed product
  curl                            issues an authenticated API request
  delete-certificate-authority    deletes a certificate authority on the Ops Manager
  delete-ssl-certificate          deletes certificate applied to Ops Manager
  diagnostic-report               reports current state of your Ops Manager
  disable-director-verifiers      disables director verifiers
  disable-product-verifiers       disables product verifiers
  errands                         list errands for a product
  expiring-certificates           lists expiring certificates from the Ops Manager targeted
  generate-certificate            generates a new certificate signed by Ops Manager's root CA
  generate-certificate-authority  generates a certificate authority on the Opsman
  import-installation             imports a given installation to the Ops Manager targeted
  installation-log                output installation logs
  installations                   list recent installation events
  interpolate                     interpolates variables into a manifest
  pre-deploy-check                checks completeness and validity of product configuration
  product-metadata                prints product metadata
  regenerate-certificates         deletes all non-configurable certificates in Ops Manager so they will automatically be regenerated on the next apply-changes
  revert-staged-changes           This command reverts the staged changes already on an Ops Manager.
  ssl-certificate                 gets certificate applied to Ops Manager
  staged-director-config          generates a config from a staged director
  tile-metadata                   **DEPRECATED** prints product metadata. Use product-metadata instead
  update-ssl-certificate          updates the SSL Certificate on the Ops Manager

```
