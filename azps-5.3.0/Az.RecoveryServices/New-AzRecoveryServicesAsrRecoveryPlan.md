---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467248"
---
# <span data-ttu-id="96a91-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96a91-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="96a91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a91-102">SYNOPSIS</span></span>
<span data-ttu-id="96a91-103">AsR helyreállítási tervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="96a91-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="96a91-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96a91-104">SYNTAX</span></span>

### <span data-ttu-id="96a91-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96a91-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a91-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="96a91-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a91-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="96a91-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a91-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="96a91-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a91-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96a91-109">DESCRIPTION</span></span>
<span data-ttu-id="96a91-110">A **New-AzRecoveryServicesAsrRecoveryPlan** parancsmag létrehoz egy Azure-webhely-helyreállítást, egy helyreállítási tervet a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="96a91-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="96a91-111">A helyreállítási tervek összegyűjtik egy egységbe az alkalmazáshoz tartozó virtuális gépeket, és lehetővé teszik számukra a közös helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="96a91-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="96a91-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96a91-112">EXAMPLES</span></span>

### <span data-ttu-id="96a91-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="96a91-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="96a91-114">Elindítja a helyreállítási terv létrehozását a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="96a91-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="96a91-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="96a91-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="96a91-116">Elindítja az Azure-zóna helyreállítási terv-létrehozási műveletét a replikált elemek zónában való létrehozásához, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="96a91-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="96a91-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96a91-117">PARAMETERS</span></span>

### <span data-ttu-id="96a91-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="96a91-118">-Azure</span></span>
<span data-ttu-id="96a91-119">A Kapcsoló paraméter az Azure-nak az Azure-beli katasztrófa-helyreállításra, a helyreállítási terv létrehozására vonatkozó forgatókönyvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="96a91-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="96a91-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="96a91-120">-AzureZoneToZone</span></span>
<span data-ttu-id="96a91-121">A Kapcsoló paraméter azt adja meg, hogy létrehozza a replikált elemet az Azure Zone-ban zóna esetében.</span><span class="sxs-lookup"><span data-stu-id="96a91-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="96a91-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a91-122">-DefaultProfile</span></span>
<span data-ttu-id="96a91-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96a91-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="96a91-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="96a91-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="96a91-125">A helyreállítási terv részét képezi a replikációval védett elemek feladatátvételi telepítési modellje (klasszikus vagy erőforrás-kezelő).</span><span class="sxs-lookup"><span data-stu-id="96a91-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="96a91-126">-Name</span><span class="sxs-lookup"><span data-stu-id="96a91-126">-Name</span></span>
<span data-ttu-id="96a91-127">A helyreállítási terv neve.</span><span class="sxs-lookup"><span data-stu-id="96a91-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="96a91-128">-Path</span><span class="sxs-lookup"><span data-stu-id="96a91-128">-Path</span></span>
<span data-ttu-id="96a91-129">A helyreállítási terv definíciójának json-fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="96a91-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="96a91-130">A helyreállítási terv meghatározására json használható a helyreállítási terv létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="96a91-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="96a91-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="96a91-131">-PrimaryFabric</span></span>
<span data-ttu-id="96a91-132">A helyreállítási terv részét képezi a replikációval védett elemek elsődleges ASR-szerkezetének ASR-anyagobjektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="96a91-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="96a91-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="96a91-133">-PrimaryZone</span></span>
<span data-ttu-id="96a91-134">A helyreállítási terv részét képezi a replikációval védett elemek elsődleges elérhetőségi zónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="96a91-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="96a91-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="96a91-135">-RecoveryFabric</span></span>
<span data-ttu-id="96a91-136">A helyreállítási terv részét képezi a replikációval védett elemek helyreállítási ASR-anyagának ASR-anyagának ASR-objektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="96a91-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="96a91-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="96a91-137">-RecoveryZone</span></span>
<span data-ttu-id="96a91-138">A helyreállítási terv részét képezi a replikációval védett elemek elsődleges elérhetőségi zónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="96a91-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="96a91-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="96a91-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="96a91-140">A helyreállítási terv első csoportjához hozzáadható replikációs védett elemek listája.</span><span class="sxs-lookup"><span data-stu-id="96a91-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="96a91-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a91-141">-Confirm</span></span>
<span data-ttu-id="96a91-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96a91-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a91-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a91-143">-WhatIf</span></span>
<span data-ttu-id="96a91-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96a91-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96a91-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96a91-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a91-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a91-146">CommonParameters</span></span>
<span data-ttu-id="96a91-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a91-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a91-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96a91-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a91-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96a91-149">INPUTS</span></span>

### <span data-ttu-id="96a91-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="96a91-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="96a91-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96a91-151">OUTPUTS</span></span>

### <span data-ttu-id="96a91-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="96a91-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="96a91-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96a91-153">NOTES</span></span>

## <span data-ttu-id="96a91-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96a91-154">RELATED LINKS</span></span>

[<span data-ttu-id="96a91-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96a91-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="96a91-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96a91-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="96a91-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96a91-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


