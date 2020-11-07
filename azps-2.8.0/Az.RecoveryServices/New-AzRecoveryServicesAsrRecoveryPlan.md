---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5e0c3627616ae7310785943f73ed7c07f0f263b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838706"
---
# <span data-ttu-id="4abb1-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4abb1-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="4abb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4abb1-102">SYNOPSIS</span></span>
<span data-ttu-id="4abb1-103">ASR-helyreállítási csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4abb1-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="4abb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4abb1-104">SYNTAX</span></span>

### <span data-ttu-id="4abb1-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4abb1-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abb1-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="4abb1-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abb1-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="4abb1-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4abb1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4abb1-108">DESCRIPTION</span></span>
<span data-ttu-id="4abb1-109">A **New-AzRecoveryServicesAsrRecoveryPlan** parancsmag az Azure webhely-helyreállítási helyreállítási csomagot hoz létre a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="4abb1-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="4abb1-110">A helyreállítási terv az alkalmazásba tartozó virtuális gépeket egy egységbe gyűjti, amely lehetővé teszi számukra a helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="4abb1-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="4abb1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4abb1-111">EXAMPLES</span></span>

### <span data-ttu-id="4abb1-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4abb1-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="4abb1-113">Elindítja a helyreállítási terv létrehozása műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4abb1-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4abb1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4abb1-114">PARAMETERS</span></span>

### <span data-ttu-id="4abb1-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="4abb1-115">-Azure</span></span>
<span data-ttu-id="4abb1-116">{{Fill Azure Description}}</span><span class="sxs-lookup"><span data-stu-id="4abb1-116">{{Fill Azure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abb1-117">-DefaultProfile</span></span>
<span data-ttu-id="4abb1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4abb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4abb1-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="4abb1-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="4abb1-120">Megadja a helyreállítási csomag részét képező replikációs telepítő modellt (klasszikus vagy erőforrás-kezelő) a replikációs védelemmel ellátott elemek között.</span><span class="sxs-lookup"><span data-stu-id="4abb1-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4abb1-121">-Name</span></span>
<span data-ttu-id="4abb1-122">A helyreállítási terv neve.</span><span class="sxs-lookup"><span data-stu-id="4abb1-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="4abb1-123">-Path</span></span>
<span data-ttu-id="4abb1-124">A helyreállítási terv definíciója JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4abb1-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="4abb1-125">A helyreállítási terv definíciója: a JSON segítségével létrehozhatja a helyreállítási tervet.</span><span class="sxs-lookup"><span data-stu-id="4abb1-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="4abb1-126">-PrimaryFabric</span></span>
<span data-ttu-id="4abb1-127">A helyreállítási csomag részét képező, a replikációs védelemmel ellátott elemek elsődleges ASR-szövetéhez tartozó ASR-szövet objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4abb1-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="4abb1-128">-RecoveryFabric</span></span>
<span data-ttu-id="4abb1-129">A helyreállítási csomag részét képező replikációs helyreállítási anyaghoz tartozó ASR-szövet objektum.</span><span class="sxs-lookup"><span data-stu-id="4abb1-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4abb1-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4abb1-131">A helyreállítási terv első csoportjához hozzáadni kívánt replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="4abb1-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4abb1-132">-Confirm</span></span>
<span data-ttu-id="4abb1-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4abb1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abb1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abb1-134">-WhatIf</span></span>
<span data-ttu-id="4abb1-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4abb1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4abb1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4abb1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abb1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abb1-137">CommonParameters</span></span>
<span data-ttu-id="4abb1-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4abb1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abb1-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abb1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abb1-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4abb1-140">INPUTS</span></span>

### <span data-ttu-id="4abb1-141">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="4abb1-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="4abb1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4abb1-142">OUTPUTS</span></span>

### <span data-ttu-id="4abb1-143">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4abb1-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4abb1-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4abb1-144">NOTES</span></span>

## <span data-ttu-id="4abb1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4abb1-145">RELATED LINKS</span></span>

[<span data-ttu-id="4abb1-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4abb1-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4abb1-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4abb1-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4abb1-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4abb1-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


