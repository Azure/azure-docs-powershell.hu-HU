---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680507"
---
# <span data-ttu-id="29552-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="29552-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="29552-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29552-102">SYNOPSIS</span></span>
<span data-ttu-id="29552-103">Információt kap a webhely-helyreállítási hálózati megfeleltetésekről az aktuális boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="29552-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29552-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29552-104">SYNTAX</span></span>

### <span data-ttu-id="29552-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29552-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="29552-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="29552-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="29552-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29552-107">DESCRIPTION</span></span>
<span data-ttu-id="29552-108">A **Get-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag információt kap az Azure webhely-helyreállítási hálózati megfeleltetésekről a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="29552-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="29552-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29552-109">EXAMPLES</span></span>

### <span data-ttu-id="29552-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29552-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="29552-111">Az átadott hálózat minden hálózati megfeleltetésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="29552-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="29552-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29552-112">PARAMETERS</span></span>

### <span data-ttu-id="29552-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29552-113">-Name</span></span>
<span data-ttu-id="29552-114">A beszerzéshez használandó ASR-hálózati megfeleltetési objektum neve.</span><span class="sxs-lookup"><span data-stu-id="29552-114">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="29552-115">– Hálózat</span><span class="sxs-lookup"><span data-stu-id="29552-115">-Network</span></span>
<span data-ttu-id="29552-116">A megadott hálózati ASR-objektumnak megfelelő ASR-hálózati megfeleltetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="29552-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29552-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29552-117">CommonParameters</span></span>
<span data-ttu-id="29552-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29552-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29552-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29552-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29552-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29552-120">INPUTS</span></span>

### <span data-ttu-id="29552-121">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="29552-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="29552-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29552-122">OUTPUTS</span></span>

### <span data-ttu-id="29552-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="29552-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="29552-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29552-124">NOTES</span></span>

## <span data-ttu-id="29552-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29552-125">RELATED LINKS</span></span>

[<span data-ttu-id="29552-126">Új – AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="29552-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="29552-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="29552-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
