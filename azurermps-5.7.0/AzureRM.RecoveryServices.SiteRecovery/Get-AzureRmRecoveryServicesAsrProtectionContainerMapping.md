---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 5d0d6bc894cd252ac36b4ceee312040a998b3857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494409"
---
# <span data-ttu-id="5875f-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5875f-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="5875f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5875f-102">SYNOPSIS</span></span>
<span data-ttu-id="5875f-103">Megkapja az Azure site Recovery Protection Container-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="5875f-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5875f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5875f-104">SYNTAX</span></span>

### <span data-ttu-id="5875f-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5875f-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5875f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="5875f-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5875f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5875f-107">DESCRIPTION</span></span>
<span data-ttu-id="5875f-108">A **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** parancsmag információkat kap a védelmi tárolóról a megadott ASR-védelmi tárolóhoz tartozó replikációs házirend-megfeleltetések (társítás) esetén.</span><span class="sxs-lookup"><span data-stu-id="5875f-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="5875f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5875f-109">EXAMPLES</span></span>

### <span data-ttu-id="5875f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5875f-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="5875f-111">A tárolóhoz tartozó védelmi tárolók megfeleltetésének listája.</span><span class="sxs-lookup"><span data-stu-id="5875f-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="5875f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="5875f-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="5875f-113">A megadott védelmi tároló minden védelmi tárolójának megfeleltetése.</span><span class="sxs-lookup"><span data-stu-id="5875f-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="5875f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5875f-114">PARAMETERS</span></span>

### <span data-ttu-id="5875f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5875f-115">-DefaultProfile</span></span>
<span data-ttu-id="5875f-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5875f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="5875f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5875f-117">-Name</span></span>
<span data-ttu-id="5875f-118">Megadja a beszerzéshez tartozó védelmi tároló megfeleltetésének nevét.</span><span class="sxs-lookup"><span data-stu-id="5875f-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="5875f-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5875f-119">-ProtectionContainer</span></span>
<span data-ttu-id="5875f-120">A megadott ASR-védelmi tároló objektumnak megfelelő védelmi tároló megfeleltetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="5875f-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5875f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5875f-121">CommonParameters</span></span>
<span data-ttu-id="5875f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5875f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5875f-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5875f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5875f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5875f-124">INPUTS</span></span>

### <span data-ttu-id="5875f-125">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5875f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="5875f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5875f-126">OUTPUTS</span></span>

### <span data-ttu-id="5875f-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5875f-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5875f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5875f-128">NOTES</span></span>

## <span data-ttu-id="5875f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5875f-129">RELATED LINKS</span></span>

[<span data-ttu-id="5875f-130">Új – AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5875f-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="5875f-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5875f-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
