---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503983"
---
# <span data-ttu-id="a428c-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a428c-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="a428c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a428c-102">SYNOPSIS</span></span>
<span data-ttu-id="a428c-103">A rendelkezésre álló (észlelt) ASR-tárolók besorolását a helyreállítási szolgáltatások pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="a428c-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a428c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a428c-104">SYNTAX</span></span>

### <span data-ttu-id="a428c-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a428c-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="a428c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a428c-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="a428c-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a428c-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="a428c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a428c-108">DESCRIPTION</span></span>
<span data-ttu-id="a428c-109">A **Get-AzureRmRecoveryServicesAsrStorageClassification** parancsmag részletesen ismerteti a helyreállítási szolgáltatások tárolójában felfedezett ASR-tárolási besorolásokat.</span><span class="sxs-lookup"><span data-stu-id="a428c-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="a428c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a428c-110">EXAMPLES</span></span>

### <span data-ttu-id="a428c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a428c-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="a428c-112">A megadott ASR-anyagnak megfelelő észlelt tárolási besorolások listája.</span><span class="sxs-lookup"><span data-stu-id="a428c-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="a428c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a428c-113">PARAMETERS</span></span>

### <span data-ttu-id="a428c-114">-Szövet</span><span class="sxs-lookup"><span data-stu-id="a428c-114">-Fabric</span></span>
<span data-ttu-id="a428c-115">Egy ASR-szövet objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a428c-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="a428c-116">A parancsmag a megadott ASR-anyaghoz tartozó, felfedezett tárolási kategóriák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a428c-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a428c-117">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="a428c-117">-FriendlyName</span></span>
<span data-ttu-id="a428c-118">A beolvasott tárterület-besorolási objektum rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a428c-118">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a428c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a428c-119">-Name</span></span>
<span data-ttu-id="a428c-120">A beolvasott tárterület-osztályozási objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a428c-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="a428c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a428c-121">CommonParameters</span></span>
<span data-ttu-id="a428c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a428c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a428c-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a428c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a428c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a428c-124">INPUTS</span></span>

### <span data-ttu-id="a428c-125">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a428c-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a428c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a428c-126">OUTPUTS</span></span>

### <span data-ttu-id="a428c-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a428c-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a428c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a428c-128">NOTES</span></span>

## <span data-ttu-id="a428c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a428c-129">RELATED LINKS</span></span>

