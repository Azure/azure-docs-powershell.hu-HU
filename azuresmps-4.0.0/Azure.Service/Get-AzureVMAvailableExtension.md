---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016544"
---
# <span data-ttu-id="20e40-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="20e40-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="20e40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20e40-102">SYNOPSIS</span></span>
<span data-ttu-id="20e40-103">Információt kap a virtuális gépekhez elérhető legújabb bővítményekről.</span><span class="sxs-lookup"><span data-stu-id="20e40-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="20e40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20e40-104">SYNTAX</span></span>

### <span data-ttu-id="20e40-105">ListLatestExtensions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20e40-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="20e40-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="20e40-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="20e40-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="20e40-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="20e40-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="20e40-108">DESCRIPTION</span></span>
<span data-ttu-id="20e40-109">A **Get-AzureVMAvailableExtension** parancsmag információt kap a virtuális gépekhez elérhető legújabb bővítményekről.</span><span class="sxs-lookup"><span data-stu-id="20e40-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="20e40-110">Példák</span><span class="sxs-lookup"><span data-stu-id="20e40-110">EXAMPLES</span></span>

### <span data-ttu-id="20e40-111">1. példa: információk beszerzése a legújabb elérhető bővítményekhez</span><span class="sxs-lookup"><span data-stu-id="20e40-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="20e40-112">Ez a parancs információkat kap az összes virtuális gépen elérhető legújabb bővítményekről.</span><span class="sxs-lookup"><span data-stu-id="20e40-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="20e40-113">2. példa: adatok beolvasása meghatározott kiterjesztési névvel</span><span class="sxs-lookup"><span data-stu-id="20e40-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="20e40-114">Ez a parancs információt kap a VMAccessAgent nevű bővítmény összes verziójáról, valamint a Microsoft. Computer nevű közzétevőről.</span><span class="sxs-lookup"><span data-stu-id="20e40-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="20e40-115">3. példa: adatok beolvasása egy adott virtuálisgép-bővítményből verziószám alapján</span><span class="sxs-lookup"><span data-stu-id="20e40-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="20e40-116">Ez a parancs információkat kap a VMAccessAgent nevű bővítményről és a Microsoft. számításról a 1.0.3 kiterjesztésű verzióhoz.</span><span class="sxs-lookup"><span data-stu-id="20e40-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="20e40-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20e40-117">PARAMETERS</span></span>

### <span data-ttu-id="20e40-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="20e40-118">-AllVersions</span></span>
<span data-ttu-id="20e40-119">Azt jelzi, hogy ez a parancsmag a bővítmény minden verzióját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="20e40-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="20e40-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="20e40-120">-ExtensionName</span></span>
<span data-ttu-id="20e40-121">A rendelkezésre álló kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20e40-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="20e40-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="20e40-122">-InformationAction</span></span>
<span data-ttu-id="20e40-123">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="20e40-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="20e40-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="20e40-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20e40-125">Folytassa</span><span class="sxs-lookup"><span data-stu-id="20e40-125">Continue</span></span>
- <span data-ttu-id="20e40-126">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="20e40-126">Ignore</span></span>
- <span data-ttu-id="20e40-127">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="20e40-127">Inquire</span></span>
- <span data-ttu-id="20e40-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20e40-128">SilentlyContinue</span></span>
- <span data-ttu-id="20e40-129">állj</span><span class="sxs-lookup"><span data-stu-id="20e40-129">Stop</span></span>
- <span data-ttu-id="20e40-130">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="20e40-130">Suspend</span></span>

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

### <span data-ttu-id="20e40-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20e40-131">-InformationVariable</span></span>
<span data-ttu-id="20e40-132">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="20e40-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20e40-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="20e40-133">-Profile</span></span>
<span data-ttu-id="20e40-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="20e40-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20e40-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="20e40-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20e40-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="20e40-136">-Publisher</span></span>
<span data-ttu-id="20e40-137">A bővítmény közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20e40-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="20e40-138">-Verzió</span><span class="sxs-lookup"><span data-stu-id="20e40-138">-Version</span></span>
<span data-ttu-id="20e40-139">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="20e40-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="20e40-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e40-140">CommonParameters</span></span>
<span data-ttu-id="20e40-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20e40-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e40-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e40-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e40-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20e40-143">INPUTS</span></span>

## <span data-ttu-id="20e40-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20e40-144">OUTPUTS</span></span>

## <span data-ttu-id="20e40-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20e40-145">NOTES</span></span>

## <span data-ttu-id="20e40-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20e40-146">RELATED LINKS</span></span>

