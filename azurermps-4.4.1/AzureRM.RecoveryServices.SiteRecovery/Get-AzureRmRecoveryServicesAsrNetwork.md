---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 3a28545958e353c5a5523e24baf20ac6bff21ef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679371"
---
# <span data-ttu-id="958e1-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="958e1-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="958e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="958e1-102">SYNOPSIS</span></span>
<span data-ttu-id="958e1-103">Információt kap a webhelyek helyreállítása által kezelt hálózatokról az aktuális boltozatra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="958e1-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="958e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="958e1-104">SYNTAX</span></span>

### <span data-ttu-id="958e1-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="958e1-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="958e1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="958e1-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="958e1-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="958e1-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="958e1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="958e1-108">DESCRIPTION</span></span>
<span data-ttu-id="958e1-109">A **Get-AzureRmRecoveryServicesAsrNetwork** parancsmag információkat kap az Azure webhely-helyreállítási hálózatról az Azure jelenlegi webhely-helyreállítási pincéjében.</span><span class="sxs-lookup"><span data-stu-id="958e1-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="958e1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="958e1-110">EXAMPLES</span></span>

### <span data-ttu-id="958e1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="958e1-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="958e1-112">Az összes ismert hálózat beolvasása a megadott anyagból.</span><span class="sxs-lookup"><span data-stu-id="958e1-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="958e1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="958e1-113">PARAMETERS</span></span>

### <span data-ttu-id="958e1-114">-Szövet</span><span class="sxs-lookup"><span data-stu-id="958e1-114">-Fabric</span></span>
<span data-ttu-id="958e1-115">ASR-szövet objektum</span><span class="sxs-lookup"><span data-stu-id="958e1-115">ASR fabric object</span></span>

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

### <span data-ttu-id="958e1-116">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="958e1-116">-FriendlyName</span></span>
<span data-ttu-id="958e1-117">A hálózati ASR-objektum rövid neve.</span><span class="sxs-lookup"><span data-stu-id="958e1-117">Friendly name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958e1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="958e1-118">-Name</span></span>
<span data-ttu-id="958e1-119">Hálózati ASR-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="958e1-119">Name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958e1-120">CommonParameters</span></span>
<span data-ttu-id="958e1-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="958e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958e1-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958e1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958e1-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="958e1-123">INPUTS</span></span>

### <span data-ttu-id="958e1-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="958e1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="958e1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="958e1-125">OUTPUTS</span></span>

### <span data-ttu-id="958e1-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="958e1-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="958e1-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="958e1-127">NOTES</span></span>

## <span data-ttu-id="958e1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="958e1-128">RELATED LINKS</span></span>

