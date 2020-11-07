---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679370"
---
# <span data-ttu-id="ab616-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ab616-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="ab616-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab616-102">SYNOPSIS</span></span>
<span data-ttu-id="ab616-103">A helyreállítási szolgáltatások boltozatához regisztrált ASR-helyreállítási szolgáltató adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab616-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab616-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab616-104">SYNTAX</span></span>

### <span data-ttu-id="ab616-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab616-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="ab616-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ab616-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="ab616-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ab616-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## <span data-ttu-id="ab616-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab616-108">DESCRIPTION</span></span>
<span data-ttu-id="ab616-109">A **Get-AzureRmRecoveryServicesAsrServicesProvider** parancsmag információt kap az Azure webhely-helyreállítási szolgáltatónál a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="ab616-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="ab616-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ab616-110">EXAMPLES</span></span>

### <span data-ttu-id="ab616-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ab616-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="ab616-112">Felsorolja az összes ASR-replikációs szolgáltatót, amely a megadott anyagnak megfelelő helyreállítási szolgáltatások boltozatához van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="ab616-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="ab616-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab616-113">PARAMETERS</span></span>

### <span data-ttu-id="ab616-114">-Szövet</span><span class="sxs-lookup"><span data-stu-id="ab616-114">-Fabric</span></span>
<span data-ttu-id="ab616-115">Az ASR-szerkezet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab616-115">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="ab616-116">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="ab616-116">-FriendlyName</span></span>
<span data-ttu-id="ab616-117">Az ASR-helyreállítási szolgáltató rövid nevét adja meg, amelyből részletesen tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="ab616-117">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="ab616-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab616-118">-Name</span></span>
<span data-ttu-id="ab616-119">Annak az ASR-helyreállítási szolgáltatónak a nevét adja meg, amelyről részleteket szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="ab616-119">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="ab616-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab616-120">CommonParameters</span></span>
<span data-ttu-id="ab616-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab616-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab616-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab616-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab616-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab616-123">INPUTS</span></span>

### <span data-ttu-id="ab616-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ab616-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ab616-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab616-125">OUTPUTS</span></span>

### <span data-ttu-id="ab616-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ab616-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ab616-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab616-127">NOTES</span></span>

## <span data-ttu-id="ab616-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab616-128">RELATED LINKS</span></span>

[<span data-ttu-id="ab616-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ab616-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="ab616-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ab616-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
