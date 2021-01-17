---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468746"
---
# <span data-ttu-id="dac75-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dac75-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="dac75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dac75-102">SYNOPSIS</span></span>
<span data-ttu-id="dac75-103">Létrehozza az Azure Site Recovery Protection tároló megfeleltetését úgy, hogy társítja a megadott replikációs házirendet a megadott ASR védelmi tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="dac75-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="dac75-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dac75-104">SYNTAX</span></span>

### <span data-ttu-id="dac75-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dac75-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dac75-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="dac75-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dac75-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dac75-107">DESCRIPTION</span></span>
<span data-ttu-id="dac75-108">A **New-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag létrehoz egy Azure Site Recovery Protection Container megfeleltetést úgy, hogy társítja a megadott replikációs házirendet a megadott védelmi tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="dac75-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="dac75-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dac75-109">EXAMPLES</span></span>

### <span data-ttu-id="dac75-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="dac75-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="dac75-111">Elindítja a védelmi tároló megfeleltetésének létrehozását a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="dac75-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dac75-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="dac75-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="dac75-113">Elindítja a védelmi tároló megfeleltetésének létrehozását a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="dac75-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="dac75-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dac75-114">PARAMETERS</span></span>

### <span data-ttu-id="dac75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac75-115">-DefaultProfile</span></span>
<span data-ttu-id="dac75-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dac75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dac75-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dac75-117">-Name</span></span>
<span data-ttu-id="dac75-118">A Védelmi tároló megfeleltetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac75-118">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac75-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="dac75-119">-Policy</span></span>
<span data-ttu-id="dac75-120">A megfeleltetésben használt replikációs házirend ASR-replikációs házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac75-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dac75-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dac75-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="dac75-122">A megfeleltetésben használt elsődleges védelmi tároló ASR védelmi tárolóobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac75-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac75-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dac75-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="dac75-124">Megadja annak a helyreállítási védelmi tárolónak az ASR védelmi tárolóobjektumát, amely a megfeleltetésben használatos (nem Azure-beli helyreállítási helyre való replikálás esetén használatos).)</span><span class="sxs-lookup"><span data-stu-id="dac75-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac75-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dac75-125">-Confirm</span></span>
<span data-ttu-id="dac75-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dac75-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac75-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dac75-127">-WhatIf</span></span>
<span data-ttu-id="dac75-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dac75-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dac75-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dac75-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac75-130">CommonParameters</span></span>
<span data-ttu-id="dac75-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac75-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dac75-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac75-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dac75-133">INPUTS</span></span>

### <span data-ttu-id="dac75-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="dac75-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="dac75-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dac75-135">OUTPUTS</span></span>

### <span data-ttu-id="dac75-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="dac75-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dac75-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dac75-137">NOTES</span></span>

## <span data-ttu-id="dac75-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dac75-138">RELATED LINKS</span></span>

[<span data-ttu-id="dac75-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dac75-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="dac75-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dac75-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
