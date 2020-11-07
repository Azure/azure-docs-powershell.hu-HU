---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679369"
---
# <span data-ttu-id="d7de3-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d7de3-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="d7de3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7de3-102">SYNOPSIS</span></span>
<span data-ttu-id="d7de3-103">Az ASR-tárolók osztályozási megfeleltetésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="d7de3-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7de3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7de3-104">SYNTAX</span></span>

### <span data-ttu-id="d7de3-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7de3-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="d7de3-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d7de3-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="d7de3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7de3-107">DESCRIPTION</span></span>
<span data-ttu-id="d7de3-108">A **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** PARANCSMAG az ASR-tárolók besorolási megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d7de3-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="d7de3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d7de3-109">EXAMPLES</span></span>

### <span data-ttu-id="d7de3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d7de3-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="d7de3-111">A megadott tárterület-besorolásnak megfelelő tárolási besorolási megfeleltetések felsorolása.</span><span class="sxs-lookup"><span data-stu-id="d7de3-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="d7de3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7de3-112">PARAMETERS</span></span>

### <span data-ttu-id="d7de3-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7de3-113">-Name</span></span>
<span data-ttu-id="d7de3-114">A beszerzéshez a tárterület-osztályozási megfeleltetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7de3-114">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7de3-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="d7de3-115">-StorageClassification</span></span>
<span data-ttu-id="d7de3-116">Az ASR-tárolók osztályozási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7de3-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="d7de3-117">A parancsmag beolvassa az ASR-tárolók osztályozását, amely megfelel a megadott tárterület-besorolásnak</span><span class="sxs-lookup"><span data-stu-id="d7de3-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7de3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7de3-118">CommonParameters</span></span>
<span data-ttu-id="d7de3-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7de3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7de3-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7de3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7de3-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7de3-121">INPUTS</span></span>

### <span data-ttu-id="d7de3-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7de3-122">None</span></span>

## <span data-ttu-id="d7de3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7de3-123">OUTPUTS</span></span>

### <span data-ttu-id="d7de3-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d7de3-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d7de3-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7de3-125">NOTES</span></span>

## <span data-ttu-id="d7de3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7de3-126">RELATED LINKS</span></span>

[<span data-ttu-id="d7de3-127">Új – AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d7de3-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="d7de3-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d7de3-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
