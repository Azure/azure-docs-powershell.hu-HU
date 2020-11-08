---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186561"
---
# <span data-ttu-id="a63dc-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a63dc-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="a63dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a63dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a63dc-103">Az Azure webhely-helyreállítási védelmi tárolók megfeleltetését a megadott replikációs házirendnek a megadott ASR-védelmi tárolóhoz társításával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a63dc-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="a63dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a63dc-104">SYNTAX</span></span>

### <span data-ttu-id="a63dc-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a63dc-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63dc-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a63dc-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a63dc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a63dc-107">DESCRIPTION</span></span>
<span data-ttu-id="a63dc-108">A **New-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag létrehoz egy Azure site Recovery Protection Container-megfeleltetést úgy, hogy társítja a megadott replikációs házirendet a megadott védelmi tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="a63dc-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="a63dc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a63dc-109">EXAMPLES</span></span>

### <span data-ttu-id="a63dc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a63dc-110">Example 1</span></span>
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

<span data-ttu-id="a63dc-111">Elindítja a védett tároló megfeleltetésének létrehozását a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a63dc-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a63dc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a63dc-112">Example 2</span></span>
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

<span data-ttu-id="a63dc-113">Elindítja a védett tároló megfeleltetésének létrehozását a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a63dc-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a63dc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a63dc-114">PARAMETERS</span></span>

### <span data-ttu-id="a63dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63dc-115">-DefaultProfile</span></span>
<span data-ttu-id="a63dc-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a63dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a63dc-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a63dc-117">-Name</span></span>
<span data-ttu-id="a63dc-118">A védelmi tároló megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a63dc-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="a63dc-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a63dc-119">-Policy</span></span>
<span data-ttu-id="a63dc-120">Megadja a megfeleltetéshez használni kívánt replikációs házirendhez tartozó ASR-replikációs házirend-objektumot.</span><span class="sxs-lookup"><span data-stu-id="a63dc-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="a63dc-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a63dc-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="a63dc-122">Megadja a megfeleltetéshez használni kívánt elsődleges védelmi tárolóhoz tartozó ASR-védelmi tároló objektumot.</span><span class="sxs-lookup"><span data-stu-id="a63dc-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="a63dc-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a63dc-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="a63dc-124">Az ASR-védelem tároló objektum a megfeleltetéshez használt helyreállítási védelmi tároló objektumhoz (ez akkor használatos, ha az nem Azure-helyreállítási helyre replikálódik).</span><span class="sxs-lookup"><span data-stu-id="a63dc-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="a63dc-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a63dc-125">-Confirm</span></span>
<span data-ttu-id="a63dc-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a63dc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63dc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63dc-127">-WhatIf</span></span>
<span data-ttu-id="a63dc-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a63dc-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a63dc-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a63dc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63dc-130">CommonParameters</span></span>
<span data-ttu-id="a63dc-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a63dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63dc-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a63dc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63dc-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a63dc-133">INPUTS</span></span>

### <span data-ttu-id="a63dc-134">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a63dc-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a63dc-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a63dc-135">OUTPUTS</span></span>

### <span data-ttu-id="a63dc-136">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a63dc-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a63dc-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a63dc-137">NOTES</span></span>

## <span data-ttu-id="a63dc-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a63dc-138">RELATED LINKS</span></span>

[<span data-ttu-id="a63dc-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a63dc-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="a63dc-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a63dc-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
