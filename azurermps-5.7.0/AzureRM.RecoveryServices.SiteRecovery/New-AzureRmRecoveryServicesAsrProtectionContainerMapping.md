---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 64448977a14a702d67473621e71c7740fc6f43c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679269"
---
# <span data-ttu-id="7b44d-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7b44d-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="7b44d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b44d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b44d-103">Az Azure webhely-helyreállítási védelmi tárolók megfeleltetését a megadott replikációs házirendnek a megadott ASR-védelmi tárolóhoz társításával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7b44d-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b44d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b44d-104">SYNTAX</span></span>

### <span data-ttu-id="7b44d-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b44d-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b44d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7b44d-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b44d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b44d-107">DESCRIPTION</span></span>
<span data-ttu-id="7b44d-108">A **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** parancsmag létrehoz egy Azure site Recovery Protection Container-megfeleltetést úgy, hogy társítja a megadott replikációs házirendet a megadott védelmi tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="7b44d-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="7b44d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7b44d-109">EXAMPLES</span></span>

### <span data-ttu-id="7b44d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7b44d-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

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

<span data-ttu-id="7b44d-111">Elindítja a védett tároló megfeleltetésének létrehozását a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7b44d-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7b44d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7b44d-112">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

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

<span data-ttu-id="7b44d-113">Elindítja a védett tároló megfeleltetésének létrehozását a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7b44d-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7b44d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b44d-114">PARAMETERS</span></span>

### <span data-ttu-id="7b44d-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b44d-115">-Confirm</span></span>
<span data-ttu-id="7b44d-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b44d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b44d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b44d-117">-DefaultProfile</span></span>
<span data-ttu-id="7b44d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b44d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="7b44d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b44d-119">-Name</span></span>
<span data-ttu-id="7b44d-120">A védelmi tároló megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b44d-120">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="7b44d-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="7b44d-121">-Policy</span></span>
<span data-ttu-id="7b44d-122">Megadja a megfeleltetéshez használni kívánt replikációs házirendhez tartozó ASR-replikációs házirend-objektumot.</span><span class="sxs-lookup"><span data-stu-id="7b44d-122">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b44d-123">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7b44d-123">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="7b44d-124">Megadja a megfeleltetéshez használni kívánt elsődleges védelmi tárolóhoz tartozó ASR-védelmi tároló objektumot.</span><span class="sxs-lookup"><span data-stu-id="7b44d-124">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b44d-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7b44d-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="7b44d-126">Az ASR-védelem tároló objektum a megfeleltetéshez használt helyreállítási védelmi tároló objektumhoz (ez akkor használatos, ha az nem Azure-helyreállítási helyre replikálódik).</span><span class="sxs-lookup"><span data-stu-id="7b44d-126">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b44d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b44d-127">-WhatIf</span></span>
<span data-ttu-id="7b44d-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b44d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b44d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b44d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b44d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b44d-130">CommonParameters</span></span>
<span data-ttu-id="7b44d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b44d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b44d-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b44d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b44d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b44d-133">INPUTS</span></span>

### <span data-ttu-id="7b44d-134">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="7b44d-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="7b44d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b44d-135">OUTPUTS</span></span>

### <span data-ttu-id="7b44d-136">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7b44d-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7b44d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b44d-137">NOTES</span></span>

## <span data-ttu-id="7b44d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b44d-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b44d-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7b44d-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="7b44d-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7b44d-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
