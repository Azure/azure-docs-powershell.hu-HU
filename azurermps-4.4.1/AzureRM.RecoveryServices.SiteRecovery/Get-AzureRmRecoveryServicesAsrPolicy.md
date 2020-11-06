---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504795"
---
# <span data-ttu-id="789ab-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="789ab-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="789ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="789ab-102">SYNOPSIS</span></span>
<span data-ttu-id="789ab-103">ASR-replikációs házirendek jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="789ab-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="789ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="789ab-104">SYNTAX</span></span>

### <span data-ttu-id="789ab-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="789ab-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="789ab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="789ab-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="789ab-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="789ab-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="789ab-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="789ab-108">DESCRIPTION</span></span>
<span data-ttu-id="789ab-109">A **Get-AzureRmRecoveryServicesAsrPolicy** parancsmag a konfigurált Azure-webhelyek helyreállítási replikációs házirendjeinek vagy egy adott replikációs házirendnek a neve alapján kapja meg a listát.</span><span class="sxs-lookup"><span data-stu-id="789ab-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="789ab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="789ab-110">EXAMPLES</span></span>

### <span data-ttu-id="789ab-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="789ab-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="789ab-112">A megadott néven retruns a replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="789ab-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="789ab-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="789ab-113">PARAMETERS</span></span>

### <span data-ttu-id="789ab-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="789ab-114">-FriendlyName</span></span>
<span data-ttu-id="789ab-115">Az ASR-replikációs házirend rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="789ab-115">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="789ab-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="789ab-116">-Name</span></span>
<span data-ttu-id="789ab-117">Az ASR-replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="789ab-117">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="789ab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789ab-118">CommonParameters</span></span>
<span data-ttu-id="789ab-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="789ab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789ab-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789ab-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789ab-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="789ab-121">INPUTS</span></span>

### <span data-ttu-id="789ab-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="789ab-122">None</span></span>

## <span data-ttu-id="789ab-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="789ab-123">OUTPUTS</span></span>

### <span data-ttu-id="789ab-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="789ab-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="789ab-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="789ab-125">NOTES</span></span>

## <span data-ttu-id="789ab-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="789ab-126">RELATED LINKS</span></span>

[<span data-ttu-id="789ab-127">Új – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="789ab-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="789ab-128">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="789ab-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
