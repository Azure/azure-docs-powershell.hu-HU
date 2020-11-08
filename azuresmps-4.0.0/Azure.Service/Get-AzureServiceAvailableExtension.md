---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015606"
---
# <span data-ttu-id="157c9-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="157c9-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="157c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="157c9-102">SYNOPSIS</span></span>
<span data-ttu-id="157c9-103">Információt kap a hosztolt szolgáltatások elérhető bővítményeiről.</span><span class="sxs-lookup"><span data-stu-id="157c9-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="157c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="157c9-104">SYNTAX</span></span>

### <span data-ttu-id="157c9-105">ListLatestExtensions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="157c9-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="157c9-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="157c9-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="157c9-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="157c9-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="157c9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="157c9-108">DESCRIPTION</span></span>
<span data-ttu-id="157c9-109">A **Get-AzureServiceAvailableExtension** parancsmag a hosztolt szolgáltatások legújabb elérhető bővítményeinek adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="157c9-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="157c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="157c9-110">EXAMPLES</span></span>

### <span data-ttu-id="157c9-111">Példa 1: elérhető bővítmények beszerzése</span><span class="sxs-lookup"><span data-stu-id="157c9-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="157c9-112">Ez a parancs minden elérhető bővítményt elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="157c9-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="157c9-113">2. példa: a bővítmények beszerzése egy megadott névtérben</span><span class="sxs-lookup"><span data-stu-id="157c9-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="157c9-114">Ez a parancs a megadott névtérben megadott nevű kiterjesztéseket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="157c9-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="157c9-115">3. példa: a bővítmény meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="157c9-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="157c9-116">Ez a parancs a bővítmény egy adott verziójáról nyújt tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="157c9-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="157c9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="157c9-117">PARAMETERS</span></span>

### <span data-ttu-id="157c9-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="157c9-118">-AllVersions</span></span>
<span data-ttu-id="157c9-119">Azt jelzi, hogy ez a parancsmag a bővítmény minden verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="157c9-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157c9-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="157c9-120">-ExtensionName</span></span>
<span data-ttu-id="157c9-121">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="157c9-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157c9-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="157c9-122">-InformationAction</span></span>
<span data-ttu-id="157c9-123">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="157c9-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="157c9-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="157c9-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="157c9-125">Folytassa</span><span class="sxs-lookup"><span data-stu-id="157c9-125">Continue</span></span>
- <span data-ttu-id="157c9-126">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="157c9-126">Ignore</span></span>
- <span data-ttu-id="157c9-127">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="157c9-127">Inquire</span></span>
- <span data-ttu-id="157c9-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="157c9-128">SilentlyContinue</span></span>
- <span data-ttu-id="157c9-129">állj</span><span class="sxs-lookup"><span data-stu-id="157c9-129">Stop</span></span>
- <span data-ttu-id="157c9-130">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="157c9-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157c9-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="157c9-131">-InformationVariable</span></span>
<span data-ttu-id="157c9-132">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="157c9-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157c9-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="157c9-133">-Profile</span></span>
<span data-ttu-id="157c9-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="157c9-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="157c9-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="157c9-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157c9-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="157c9-136">-ProviderNamespace</span></span>
<span data-ttu-id="157c9-137">A bővítmény-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="157c9-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157c9-138">-Verzió</span><span class="sxs-lookup"><span data-stu-id="157c9-138">-Version</span></span>
<span data-ttu-id="157c9-139">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="157c9-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157c9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157c9-140">CommonParameters</span></span>
<span data-ttu-id="157c9-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="157c9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157c9-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="157c9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157c9-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="157c9-143">INPUTS</span></span>

## <span data-ttu-id="157c9-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="157c9-144">OUTPUTS</span></span>

## <span data-ttu-id="157c9-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="157c9-145">NOTES</span></span>

## <span data-ttu-id="157c9-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="157c9-146">RELATED LINKS</span></span>

[<span data-ttu-id="157c9-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="157c9-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


