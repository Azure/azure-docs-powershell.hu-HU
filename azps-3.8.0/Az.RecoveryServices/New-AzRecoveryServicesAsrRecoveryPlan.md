---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 851f9d52b3247fed0755b4567e3c463b1202c34b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014688"
---
# <span data-ttu-id="8b7b4-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8b7b4-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="8b7b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b7b4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7b4-103">ASR-helyreállítási csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="8b7b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b7b4-104">SYNTAX</span></span>

### <span data-ttu-id="8b7b4-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b7b4-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7b4-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="8b7b4-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7b4-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="8b7b4-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b7b4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b7b4-108">DESCRIPTION</span></span>
<span data-ttu-id="8b7b4-109">A **New-AzRecoveryServicesAsrRecoveryPlan** parancsmag létrehoz egy Azure site Recovery (helyreállítási csomag) szolgáltatást a helyreállítási szolgáltatások Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="8b7b4-110">A helyreállítási terv az alkalmazásba tartozó virtuális gépeket egy egységbe gyűjti, amely lehetővé teszi számukra a helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="8b7b4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8b7b4-111">EXAMPLES</span></span>

### <span data-ttu-id="8b7b4-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8b7b4-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="8b7b4-113">Elindítja a helyreállítási terv létrehozása műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8b7b4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b7b4-114">PARAMETERS</span></span>

### <span data-ttu-id="8b7b4-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="8b7b4-115">-Azure</span></span>
<span data-ttu-id="8b7b4-116">Kapcsoló paraméter adja meg az Azure által az Azure katasztrófa-helyreállítási, helyreállítási terv létrehozása esetét.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-116">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="8b7b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7b4-117">-DefaultProfile</span></span>
<span data-ttu-id="8b7b4-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8b7b4-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="8b7b4-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="8b7b4-120">Megadja a helyreállítási csomag részét képező replikációs telepítő modellt (klasszikus vagy erőforrás-kezelő) a replikációs védelemmel ellátott elemek között.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8b7b4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b7b4-121">-Name</span></span>
<span data-ttu-id="8b7b4-122">A helyreállítási terv neve.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-122">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="8b7b4-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8b7b4-123">-Path</span></span>
<span data-ttu-id="8b7b4-124">A helyreállítási terv definíciója JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="8b7b4-125">A helyreállítási terv definíciója: a JSON segítségével létrehozhatja a helyreállítási tervet.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="8b7b4-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="8b7b4-126">-PrimaryFabric</span></span>
<span data-ttu-id="8b7b4-127">A helyreállítási csomag részét képező, a replikációs védelemmel ellátott elemek elsődleges ASR-szövetéhez tartozó ASR-szövet objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8b7b4-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8b7b4-128">-RecoveryFabric</span></span>
<span data-ttu-id="8b7b4-129">A helyreállítási csomag részét képező replikációs helyreállítási anyaghoz tartozó ASR-szövet objektum.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="8b7b4-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8b7b4-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8b7b4-131">A helyreállítási terv első csoportjához hozzáadni kívánt replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="8b7b4-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b7b4-132">-Confirm</span></span>
<span data-ttu-id="8b7b4-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b7b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7b4-134">-WhatIf</span></span>
<span data-ttu-id="8b7b4-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b7b4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b7b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7b4-137">CommonParameters</span></span>
<span data-ttu-id="8b7b4-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b7b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7b4-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b7b4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7b4-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b7b4-140">INPUTS</span></span>

### <span data-ttu-id="8b7b4-141">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="8b7b4-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="8b7b4-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b7b4-142">OUTPUTS</span></span>

### <span data-ttu-id="8b7b4-143">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8b7b4-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8b7b4-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b7b4-144">NOTES</span></span>

## <span data-ttu-id="8b7b4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b7b4-145">RELATED LINKS</span></span>

[<span data-ttu-id="8b7b4-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8b7b4-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8b7b4-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8b7b4-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8b7b4-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8b7b4-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


