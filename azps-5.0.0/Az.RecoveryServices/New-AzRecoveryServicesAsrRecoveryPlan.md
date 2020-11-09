---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301196"
---
# <span data-ttu-id="7de59-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7de59-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="7de59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7de59-102">SYNOPSIS</span></span>
<span data-ttu-id="7de59-103">ASR-helyreállítási csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7de59-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="7de59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7de59-104">SYNTAX</span></span>

### <span data-ttu-id="7de59-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7de59-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de59-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7de59-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de59-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="7de59-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de59-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="7de59-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de59-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7de59-109">DESCRIPTION</span></span>
<span data-ttu-id="7de59-110">A **New-AzRecoveryServicesAsrRecoveryPlan** parancsmag létrehoz egy Azure site Recovery (helyreállítási csomag) szolgáltatást a helyreállítási szolgáltatások Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="7de59-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="7de59-111">A helyreállítási terv az alkalmazásba tartozó virtuális gépeket egy egységbe gyűjti, amely lehetővé teszi számukra a helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="7de59-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="7de59-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7de59-112">EXAMPLES</span></span>

### <span data-ttu-id="7de59-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7de59-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="7de59-114">Elindítja a helyreállítási terv létrehozása műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7de59-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7de59-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="7de59-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="7de59-116">Elindítja az Azure-zóna helyreállítási terv létrehozásának műveletét a replikált elemek zónájába, és a művelet nyomon követéséhez használt ASR-feladatot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7de59-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7de59-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7de59-117">PARAMETERS</span></span>

### <span data-ttu-id="7de59-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="7de59-118">-Azure</span></span>
<span data-ttu-id="7de59-119">Kapcsoló paraméter adja meg az Azure által az Azure katasztrófa-helyreállítási, helyreállítási terv létrehozása esetét.</span><span class="sxs-lookup"><span data-stu-id="7de59-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="7de59-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="7de59-120">-AzureZoneToZone</span></span>
<span data-ttu-id="7de59-121">A kapcsoló paraméter a replikált elem létrehozásának lépéseit adja meg az Azure Zone-ban.</span><span class="sxs-lookup"><span data-stu-id="7de59-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de59-122">-DefaultProfile</span></span>
<span data-ttu-id="7de59-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7de59-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7de59-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="7de59-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="7de59-125">Megadja a helyreállítási csomag részét képező replikációs telepítő modellt (klasszikus vagy erőforrás-kezelő) a replikációs védelemmel ellátott elemek között.</span><span class="sxs-lookup"><span data-stu-id="7de59-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="7de59-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7de59-126">-Name</span></span>
<span data-ttu-id="7de59-127">A helyreállítási terv neve.</span><span class="sxs-lookup"><span data-stu-id="7de59-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de59-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="7de59-128">-Path</span></span>
<span data-ttu-id="7de59-129">A helyreállítási terv definíciója JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7de59-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="7de59-130">A helyreállítási terv definíciója: a JSON segítségével létrehozhatja a helyreállítási tervet.</span><span class="sxs-lookup"><span data-stu-id="7de59-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="7de59-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="7de59-131">-PrimaryFabric</span></span>
<span data-ttu-id="7de59-132">A helyreállítási csomag részét képező, a replikációs védelemmel ellátott elemek elsődleges ASR-szövetéhez tartozó ASR-szövet objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7de59-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de59-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="7de59-133">-PrimaryZone</span></span>
<span data-ttu-id="7de59-134">Megadja a helyreállítási terv részét képező replikációs védelemmel ellátott elemek elsődleges elérhetőség-zónáját.</span><span class="sxs-lookup"><span data-stu-id="7de59-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de59-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="7de59-135">-RecoveryFabric</span></span>
<span data-ttu-id="7de59-136">A helyreállítási csomag részét képező replikációs helyreállítási anyaghoz tartozó ASR-szövet objektum.</span><span class="sxs-lookup"><span data-stu-id="7de59-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="7de59-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="7de59-137">-RecoveryZone</span></span>
<span data-ttu-id="7de59-138">Megadja a helyreállítási terv részét képező replikációs védelemmel ellátott elemek elsődleges elérhetőség-zónáját.</span><span class="sxs-lookup"><span data-stu-id="7de59-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de59-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7de59-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7de59-140">A helyreállítási terv első csoportjához hozzáadni kívánt replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="7de59-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de59-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7de59-141">-Confirm</span></span>
<span data-ttu-id="7de59-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7de59-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de59-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de59-143">-WhatIf</span></span>
<span data-ttu-id="7de59-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7de59-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7de59-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7de59-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de59-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de59-146">CommonParameters</span></span>
<span data-ttu-id="7de59-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7de59-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de59-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7de59-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de59-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7de59-149">INPUTS</span></span>

### <span data-ttu-id="7de59-150">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="7de59-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="7de59-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7de59-151">OUTPUTS</span></span>

### <span data-ttu-id="7de59-152">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7de59-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7de59-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7de59-153">NOTES</span></span>

## <span data-ttu-id="7de59-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7de59-154">RELATED LINKS</span></span>

[<span data-ttu-id="7de59-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7de59-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7de59-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7de59-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7de59-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7de59-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


