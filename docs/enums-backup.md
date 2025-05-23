```graphql
"""A provider that a system backup can be exported to."""
enum SystemBackupDestinationProvider {
  """Azure Blob Storage"""
  AZURE_BLOB_STORAGE
  """Amazon S3"""
  AWS_S3
  """DigitalOcean Spaces"""
  DIGITALOCEAN_SPACES
  """Scaleway Object Storage"""
  SCALEWAY_OBJECT_STORAGE
  """Dropbox"""
  DROPBOX
  """Google Cloud Storage"""
  GOOGLE_CLOUD_STORAGE
  """SFTP"""
  SFTP
}

"""
The name of a credential used to authenticate against configured destinations to export system backups to.
"""
enum SystemBackupDestinationProviderCredential {
  """Your account name."""
  AZURE_BLOB_STORAGE_ACCOUNT_NAME
  """Your account key."""
  AZURE_BLOB_STORAGE_ACCOUNT_KEY
  """The container name."""
  AZURE_BLOB_STORAGE_CONTAINER_NAME
  """Your AWS S3 account key."""
  AWS_S3_KEY
  """Your AWS S3 account secret."""
  AWS_S3_SECRET
  """Your AWS S3 region."""
  AWS_S3_REGION
  """The AWS S3 API version."""
  AWS_S3_VERSION
  """Your AWS S3 bucket."""
  AWS_S3_BUCKET_NAME
  """Your DigitalOcean Spaces account key."""
  DIGITALOCEAN_SPACES_KEY
  """Your DigitalOcean Spaces account secret."""
  DIGITALOCEAN_SPACES_SECRET
  """Your DigitalOcean Spaces region."""
  DIGITALOCEAN_SPACES_REGION
  """The DigitalOcean Spaces API version."""
  DIGITALOCEAN_SPACES_VERSION
  """The DigitalOcean Spaces endpoint."""
  DIGITALOCEAN_SPACES_ENDPOINT
  """Your DigitalOcean Spaces bucket."""
  DIGITALOCEAN_SPACES_BUCKET_NAME
  """Your Scaleway Object Storage account key."""
  SCALEWAY_OBJECT_STORAGE_KEY
  """Your Scaleway Object Storage account secret."""
  SCALEWAY_OBJECT_STORAGE_SECRET
  """Your Scaleway Object Storage region."""
  SCALEWAY_OBJECT_STORAGE_REGION
  """The Scaleway Object Storage API version."""
  SCALEWAY_OBJECT_STORAGE_VERSION
  """The Scaleway Object Storage endpoint."""
  SCALEWAY_OBJECT_STORAGE_ENDPOINT
  """Your Scaleway Object Storage bucket."""
  SCALEWAY_OBJECT_STORAGE_BUCKET_NAME
  """Your Dropbox account authorization token."""
  DROPBOX_AUTHORIZATION_TOKEN
  """Your Google project ID."""
  GOOGLE_CLOUD_STORAGE_PROJECT_ID
  """The contents of your key file."""
  GOOGLE_CLOUD_STORAGE_KEY_FILE_CONTENTS
  """Your Google Cloud Storage bucket."""
  GOOGLE_CLOUD_STORAGE_BUCKET_NAME
  """The host of the SFTP server."""
  SFTP_HOST
  """The port of the SFTP server."""
  SFTP_PORT
  """Your SFTP username."""
  SFTP_USERNAME
  """Your SFTP password."""
  SFTP_PASSWORD
}

"""The status of an export attempt of a system backup."""
enum SystemBackupExportStatus {
  """The export of the system backup is pending."""
  PENDING
  """The export of the system backup has successfully completed."""
  SUCCESSFUL
  """The export of the system backup has failed."""
  FAILED
}

"""The status of a system backup"""
enum SystemBackupStatus {
  """The system backup is pending."""
  PENDING
  """The system backup is running."""
  IN_PROGRESS
  """The system backup has successfully completed."""
  SUCCESSFUL
  """The system backup has failed."""
  FAILED
}
```
