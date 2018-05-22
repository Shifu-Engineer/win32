---
Description: 'The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate to provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.'
ms.assetid: 'd53107b7-a153-41cf-9876-1d28aaf99816'
title: Extension Functions
---

# Extension Functions

The [*X.509*](https://msdn.microsoft.com/library/windows/desktop/ms721636#-security-x-509-gly) version 3 certificate format identifies multiple extensions that can be added to a certificate to provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.

CertEnroll.dll implements the following interfaces to manage certificate extensions:

-   [**IX509Extension**](ix509extension.md)
-   [**IX509Extensions**](ix509extensions.md)
-   [**IX509ExtensionAlternativeNames**](ix509extensionalternativenames.md)
-   [**IX509ExtensionAuthorityKeyIdentifier**](ix509extensionauthoritykeyidentifier.md)
-   [**IX509ExtensionBasicConstraints**](ix509extensionbasicconstraints.md)
-   [**IX509ExtensionCertificatePolicies**](ix509extensioncertificatepolicies.md)
-   [**IX509ExtensionEnhancedKeyUsage**](ix509extensionenhancedkeyusage.md)
-   [**IX509ExtensionKeyUsage**](ix509extensionkeyusage.md)
-   [**IX509ExtensionMSApplicationPolicies**](ix509extensionmsapplicationpolicies.md)
-   [**IX509ExtensionSmimeCapabilities**](ix509extensionsmimecapabilities.md)
-   [**IX509ExtensionSubjectKeyIdentifier**](ix509extensionsubjectkeyidentifier.md)
-   [**IX509ExtensionTemplate**](ix509extensiontemplate.md)
-   [**IX509ExtensionTemplateName**](ix509extensiontemplatename.md)

Each of the following sections discusses a function exported by Xenroll.dll to manage certificate extensions. Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists:

-   [AddCertTypeToRequestWStr](#addcerttypetorequestwstr)
-   [AddCertTypeToRequestWStrEx](#addcerttypetorequestwstrex)
-   [AddExtensionsToRequest](#addextensionstorequest)
-   [addExtensionToRequestWStr](#addextensiontorequestwstr)
-   [EnableSMIMECapabilities](#enablesmimecapabilities)
-   [IncludeSubjectKeyID](#includesubjectkeyid)
-   [resetExtensions](#resetextensions)
-   [Related topics](#related-topics)

## AddCertTypeToRequestWStr

The [**AddCertTypeToRequestWStr**](https://msdn.microsoft.com/library/windows/desktop/aa385512) function in Xenroll.dll adds a certificate template, by name, to a request.

Using CertEnroll.dll, the preferred method to incorporate a template into a certificate request is to use the [**InitializeFromTemplateName**](ix509certificaterequestpkcs10-initializefromtemplatename-method.md) method on a PKCS\#10 or [*PKCS ) request object or the [**InitializeFromInnerRequestTemplateName**](ix509certificaterequestcmc-initializefrominnerrequesttemplatename.md) method on a CMC request.

If a specific template is not available on the client but is expected to be understood by the [*certification authority*](https://msdn.microsoft.com/library/windows/desktop/ms721572#-security-certification-authority-gly) (CA), you can use the [**IX509ExtensionTemplateName**](ix509extensiontemplatename.md) interface to add a version 1 template or you can use the [**IX509ExtensionTemplate**](ix509extensiontemplate.md) interface to add a version 2 template to a certificate request. For example, to add a version 1 template, perform the following actions:

1.  Create an [**IX509Extensions**](ix509extensions.md) object.
2.  Create an [**IX509ExtensionTemplateName**](ix509extensiontemplatename.md) object and call the [**InitializeEncode**](ix509extensiontemplatename-initializeencode-method.md) method, specifying the template name.
3.  Add the extension created to the [**IX509Extensions**](ix509extensions.md) collection by calling the [**Add**](ix509extensions-add-method.md) method.
4.  Create an [**IX509AttributeExtensions**](ix509attributeextensions.md) object and call the [**InitializeEncode**](ix509attributeextensions-initializeencode-method.md) method, specifying the [**IX509Extensions**](ix509extensions.md) collection on input.
5.  Retrieve an [**ICryptAttributes**](icryptattributes.md) collection object by calling the [**CryptAttributes**](ix509certificaterequestpkcs10-cryptattributes-property.md) property on an existing [**IX509CertificateRequestPkcs10**](ix509certificaterequestpkcs10.md) or [**IX509CertificateRequestCmc**](ix509certificaterequestcmc.md) request object.

## AddCertTypeToRequestWStrEx

The [**AddCertTypeToRequestWStrEx**](https://msdn.microsoft.com/library/windows/desktop/aa385513) function in Xenroll.dll adds a certificate template to a request by name, object identifier, and version.

For information about how to use CertEnroll.dll to incorporate template information in a request, see AddCertTypeToRequestWStr.

## AddExtensionsToRequest

The [**AddExtensionsToRequest**](https://msdn.microsoft.com/library/windows/desktop/aa385516) function in Xenroll.dll adds a collection of extensions to a request.

In CertEnroll.dll, extensions are added to the attributes collection of a CMC or a PKCS \#10 request. To add extensions, perform the following actions:

1.  Create an [**IX509Extensions**](ix509extensions.md) object.
2.  Create an [**IX509Extension**](ix509extension.md) object and call the [**Initialize**](ix509extension-initialize-method.md) method to create an extension from an object identifier and extension value or use any of the interfaces listed earlier to define one of the more common extensions.
3.  Add each new extension created in the preceding step to the [**IX509Extensions**](ix509extensions.md) collection by calling the [**Add**](ix509extensions-add-method.md) method.

## addExtensionToRequestWStr

The [**addExtensionToRequestWStr**](https://msdn.microsoft.com/library/windows/desktop/aa385518) function in Xenroll.dll adds a specific extension to the request.

In CertEnroll.dll, a specific extension must be defined and added to an extensions collection before the extension collection is added to the attributes collection of a CMC or a PKCS \#10 request. For more information see the AddExtensionsToRequest discussion above.

## EnableSMIMECapabilities

The [**EnableSMIMECapabilities**](https://msdn.microsoft.com/library/windows/desktop/aa385560) function in Xenroll.dll specifies or retrieves a Boolean value that indicates whether to add the **SMIMECapabilities** extension to the request.

You can call the [**SmimeCapabilities**](ix509certificaterequestpkcs10-smimecapabilities-property.md) property on the [**IX509CertificateRequestPkcs10**](ix509certificaterequestpkcs10.md) object to automatically add an [**IX509ExtensionSmimeCapabilities**](ix509extensionsmimecapabilities.md) object to the request before encoding.

## IncludeSubjectKeyID

The [**IncludeSubjectKeyID**](https://msdn.microsoft.com/library/windows/desktop/aa385628) function in Xenroll.dll specifies or retrieves a Boolean value that indicates whether to add the **SubjectKeyIdentifier** extension to the request.

By default, the **SubjectKeyIdentifier** extension is created when the [**IX509CertificateRequestPkcs10**](ix509certificaterequestpkcs10.md) request object is initialized. You can override this behavior by calling the [**SuppressOids**](ix509certificaterequestpkcs10-suppressoids-property.md) property.

If you have a [*public/private key pair*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-public-private-key-pair-gly), you can also use the [**IX509ExtensionSubjectKeyIdentifier**](ix509extensionsubjectkeyidentifier.md) interface in CertEnroll.dll to add a **SubjectKeyIdentifier** extension to a certificate request by performing the following actions:

1.  Create an [**IX509Extensions**](ix509extensions.md) object.
2.  Create an [**IX509ExtensionSubjectKeyIdentifier**](ix509extensionsubjectkeyidentifier.md) object and call the [**InitializeEncode**](ix509extensionsubjectkeyidentifier-initializeencode-method.md) method, specifying a string that contains the identifier. Typically, this is a 20-byte SHA-1 hash of the [*public key*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-public-key-gly) contained in the CA signing certificate.
3.  Add the extension created to the [**IX509Extensions**](ix509extensions.md) collection by calling the [**Add**](ix509extensions-add-method.md) method.
4.  Create an [**IX509AttributeExtensions**](ix509attributeextensions.md) object and call the [**InitializeEncode**](ix509attributeextensions-initializeencode-method.md) method, specifying the [**IX509Extensions**](ix509extensions.md) collection on input.
5.  Retrieve an [**ICryptAttributes**](icryptattributes.md) collection object by calling the [**CryptAttributes**](ix509certificaterequestpkcs10-cryptattributes-property.md) property on an existing [**IX509CertificateRequestPkcs10**](ix509certificaterequestpkcs10.md) or [**IX509CertificateRequestCmc**](ix509certificaterequestcmc.md) request object.

## resetExtensions

The [**resetExtensions**](https://msdn.microsoft.com/library/windows/desktop/aa385694) function in Xenroll.dll removes the extension collection from the request.

To remove an extension from a request by index number using CertEnroll.dll, call the [**Remove**](ix509extensions-remove-method.md) method on the [**IX509Extensions**](ix509extensions.md) collection. To remove all attributes from a request, call the [**Clear**](ix509extensions-clear-method.md) method.

## Related topics

<dl> <dt>

[Mapping Xenroll.dll to CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttributes**](icryptattributes.md)
</dt> <dt>

[**IX509Extension**](ix509extension.md)
</dt> <dt>

[**IX509Extensions**](ix509extensions.md)
</dt> </dl>

 

 


