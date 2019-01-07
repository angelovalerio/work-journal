```
{
  UI: {
    perComponent: {
      isLoading,
      error,
      element,
    }
  },
  data: {
    auth,
    employee,
    company,
    workers,
    locations,
    template: {
      id,
      groups,
      ...
    }
  }
}
```

Example: `Template`
{
  UI {
    template: {
      isLoading,
      isSignatureModalVisisble,
      lists {
        isLoading,
        error,
      }
      submitRequest {
        isLoading,
        error,
        success
      }
      sections {
        [sectionId/Index] {

        }
      }
    }
  }
  data {
    template {
      lists,
      images,
      signatures,
      details {
        id,
        syncHandler,
        subscribed,
        createdOn,
        lastModifiedOn,
        createdBy,
        lastModifiedBy,
        isDeleted,
        documentTemplateId,
        name,
        type,
        hidden,
        canDuplicate,
        isPrivate,
        creatingCompanyId,
        cellName,
        isResource,
        isFollowup,
        data: {
          title,
          signaturesInPdf,
          pdfGeneratorVersion,
          pdfCacheBuster,
          imageId,
          comments,
          groups: {
            [groupId/index] {
              groupId,
              title,
              collapsible,
              repeatable,
              isRepeat,
              isReplica,
              numberOfTimesRepeated,
              connectingId
              snapshotId,
              system,
              items {
                [itemId/index] {
                  itemId,
                  content,
                  type,
                  fileItemInfo,
                  value,
                  comments,
                  required,
                  error
                }
              }
            }
          }
        }
      }
    }
  }
}

