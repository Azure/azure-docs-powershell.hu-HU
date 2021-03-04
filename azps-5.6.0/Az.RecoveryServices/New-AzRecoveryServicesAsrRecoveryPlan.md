---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 41d023abbb1eb4453b295e64d1ccfc3b146fb197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935554"
---
# <span data-ttu-id="5e4a4-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e4a4-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="5e4a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4a4-103">AsR helyreállítási tervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="5e4a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e4a4-104">SYNTAX</span></span>

### <span data-ttu-id="5e4a4-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e4a4-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4a4-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5e4a4-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4a4-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="5e4a4-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4a4-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="5e4a4-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e4a4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e4a4-109">DESCRIPTION</span></span>
<span data-ttu-id="5e4a4-110">A **New-AzRecoveryServicesAsrRecoveryPlan** parancsmag létrehoz egy Azure-webhely-helyreállítást, egy helyreállítási tervet a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="5e4a4-111">A helyreállítási tervek összegyűjtik egy egységbe az alkalmazáshoz tartozó virtuális gépeket, és lehetővé teszik számukra a közös helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="5e4a4-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e4a4-112">EXAMPLES</span></span>

### <span data-ttu-id="5e4a4-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="5e4a4-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="5e4a4-114">Elindítja a helyreállítási terv létrehozását a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="5e4a4-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="5e4a4-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="5e4a4-116">Elindítja az Azure-zóna helyreállítási terv-létrehozási műveletét a replikált elemek zónában való létrehozásához, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5e4a4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e4a4-117">PARAMETERS</span></span>

### <span data-ttu-id="5e4a4-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="5e4a4-118">-Azure</span></span>
<span data-ttu-id="5e4a4-119">A Kapcsoló paraméter az Azure-nak az Azure-beli katasztrófa-helyreállításra, a helyreállítási terv létrehozására vonatkozó forgatókönyvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="5e4a4-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="5e4a4-120">-AzureZoneToZone</span></span>
<span data-ttu-id="5e4a4-121">A Kapcsoló paraméter azt adja meg, hogy létrehozza a replikált elemet az Azure Zone-ban zóna esetében.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="5e4a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4a4-122">-DefaultProfile</span></span>
<span data-ttu-id="5e4a4-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5e4a4-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="5e4a4-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="5e4a4-125">A helyreállítási terv részét képezi a replikációval védett elemek feladatátvételi telepítési modellje (klasszikus vagy erőforrás-kezelő).</span><span class="sxs-lookup"><span data-stu-id="5e4a4-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5e4a4-126">-Name</span></span>
<span data-ttu-id="5e4a4-127">A helyreállítási terv neve.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-128">-Path</span><span class="sxs-lookup"><span data-stu-id="5e4a4-128">-Path</span></span>
<span data-ttu-id="5e4a4-129">A helyreállítási terv definíciójának json-fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="5e4a4-130">A helyreállítási terv meghatározására json használható a helyreállítási terv létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="5e4a4-131">-PrimaryFabric</span></span>
<span data-ttu-id="5e4a4-132">A helyreállítási terv részét képezi a replikációval védett elemek elsődleges ASR-szerkezetének ASR-anyagobjektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="5e4a4-133">-PrimaryZone</span></span>
<span data-ttu-id="5e4a4-134">A helyreállítási terv részét képezi a replikációval védett elemek elsődleges elérhetőségi zónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5e4a4-135">-RecoveryFabric</span></span>
<span data-ttu-id="5e4a4-136">A helyreállítási terv részét képezi a replikációval védett elemek helyreállítási ASR-anyagának ASR-anyagának ASR-objektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="5e4a4-137">-RecoveryZone</span></span>
<span data-ttu-id="5e4a4-138">A helyreállítási terv részét képezi a replikációval védett elemek elsődleges elérhetőségi zónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e4a4-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5e4a4-140">A helyreállítási terv első csoportjához hozzáadható replikációs védett elemek listája.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="5e4a4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e4a4-141">-Confirm</span></span>
<span data-ttu-id="5e4a4-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4a4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4a4-143">-WhatIf</span></span>
<span data-ttu-id="5e4a4-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e4a4-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4a4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4a4-146">CommonParameters</span></span>
<span data-ttu-id="5e4a4-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4a4-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e4a4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4a4-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e4a4-149">INPUTS</span></span>

### <span data-ttu-id="5e4a4-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="5e4a4-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="5e4a4-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e4a4-151">OUTPUTS</span></span>

### <span data-ttu-id="5e4a4-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="5e4a4-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e4a4-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e4a4-153">NOTES</span></span>

## <span data-ttu-id="5e4a4-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e4a4-154">RELATED LINKS</span></span>

[<span data-ttu-id="5e4a4-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e4a4-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="5e4a4-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e4a4-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="5e4a4-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e4a4-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


