---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 73d57e6e73b0e7e84dd3fb8bfff04ac8705bd108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679272"
---
# <span data-ttu-id="4335c-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4335c-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="4335c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4335c-102">SYNOPSIS</span></span>
<span data-ttu-id="4335c-103">Azure site Recovery Protection tárolót hoz létre a megadott szerkezeten belül.</span><span class="sxs-lookup"><span data-stu-id="4335c-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4335c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4335c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4335c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4335c-105">DESCRIPTION</span></span>
<span data-ttu-id="4335c-106">Az New-AzureRmRecoveryServicesAsrProtectionContainer parancsmag egy védelmi tárolót hoz létre a megadott Azure webhely-helyreállítási anyagban.</span><span class="sxs-lookup"><span data-stu-id="4335c-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="4335c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4335c-107">EXAMPLES</span></span>

### <span data-ttu-id="4335c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4335c-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="4335c-109">Elindítja a védett tároló létrehozását a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4335c-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4335c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4335c-110">PARAMETERS</span></span>

### <span data-ttu-id="4335c-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4335c-111">-Confirm</span></span>
<span data-ttu-id="4335c-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4335c-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4335c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4335c-113">-DefaultProfile</span></span>
<span data-ttu-id="4335c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4335c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4335c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4335c-115">-InputObject</span></span>
<span data-ttu-id="4335c-116">Létrehozta a Replication Protection tárolót a megadott beviteli objektumban (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="4335c-116">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4335c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4335c-117">-Name</span></span>
<span data-ttu-id="4335c-118">A védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="4335c-118">Name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4335c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4335c-119">-WhatIf</span></span>
<span data-ttu-id="4335c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4335c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4335c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4335c-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4335c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4335c-122">CommonParameters</span></span>
<span data-ttu-id="4335c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4335c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4335c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4335c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4335c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4335c-125">INPUTS</span></span>

### <span data-ttu-id="4335c-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4335c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4335c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4335c-127">OUTPUTS</span></span>

### <span data-ttu-id="4335c-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4335c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4335c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4335c-129">NOTES</span></span>

## <span data-ttu-id="4335c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4335c-130">RELATED LINKS</span></span>
