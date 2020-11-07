---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 588c00dc877c4e451a4d8a0c0b44ec001b0787ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669730"
---
# <span data-ttu-id="43bbf-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="43bbf-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="43bbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="43bbf-103">Megkapja az Azure site Recovery Protection Container-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="43bbf-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="43bbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43bbf-104">SYNTAX</span></span>

### <span data-ttu-id="43bbf-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43bbf-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43bbf-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="43bbf-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43bbf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="43bbf-107">DESCRIPTION</span></span>
<span data-ttu-id="43bbf-108">A **Get-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag információkat kap a védelmi tárolóról a megadott ASR-védelmi tárolóhoz tartozó replikációs házirend-megfeleltetések (társítás) esetén.</span><span class="sxs-lookup"><span data-stu-id="43bbf-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="43bbf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="43bbf-109">EXAMPLES</span></span>

### <span data-ttu-id="43bbf-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43bbf-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="43bbf-111">A tárolóhoz tartozó védelmi tárolók megfeleltetésének listája.</span><span class="sxs-lookup"><span data-stu-id="43bbf-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="43bbf-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="43bbf-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

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

<span data-ttu-id="43bbf-113">A megadott védelmi tároló minden védelmi tárolójának megfeleltetése.</span><span class="sxs-lookup"><span data-stu-id="43bbf-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="43bbf-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43bbf-114">PARAMETERS</span></span>

### <span data-ttu-id="43bbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43bbf-115">-DefaultProfile</span></span>
<span data-ttu-id="43bbf-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43bbf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bbf-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43bbf-117">-Name</span></span>
<span data-ttu-id="43bbf-118">Megadja a beszerzéshez tartozó védelmi tároló megfeleltetésének nevét.</span><span class="sxs-lookup"><span data-stu-id="43bbf-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bbf-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="43bbf-119">-ProtectionContainer</span></span>
<span data-ttu-id="43bbf-120">A megadott ASR-védelmi tároló objektumnak megfelelő védelmi tároló megfeleltetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="43bbf-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43bbf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bbf-121">CommonParameters</span></span>
<span data-ttu-id="43bbf-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43bbf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bbf-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43bbf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bbf-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43bbf-124">INPUTS</span></span>

### <span data-ttu-id="43bbf-125">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="43bbf-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="43bbf-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43bbf-126">OUTPUTS</span></span>

### <span data-ttu-id="43bbf-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="43bbf-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="43bbf-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43bbf-128">NOTES</span></span>

## <span data-ttu-id="43bbf-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43bbf-129">RELATED LINKS</span></span>

[<span data-ttu-id="43bbf-130">Új – AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="43bbf-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="43bbf-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="43bbf-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
