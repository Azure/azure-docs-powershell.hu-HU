---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: ceedd758a660828ed3ee93390384c1e212c55097
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491872"
---
# <span data-ttu-id="04f28-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="04f28-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="04f28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04f28-102">SYNOPSIS</span></span>
<span data-ttu-id="04f28-103">ASR-helyreállítási csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04f28-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04f28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04f28-104">SYNTAX</span></span>

### <span data-ttu-id="04f28-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04f28-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f28-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="04f28-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f28-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="04f28-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f28-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="04f28-108">DESCRIPTION</span></span>
<span data-ttu-id="04f28-109">A **New-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag az Azure webhely-helyreállítási helyreállítási csomagot hoz létre a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="04f28-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="04f28-110">A helyreállítási terv az alkalmazásba tartozó virtuális gépeket egy egységbe gyűjti, amely lehetővé teszi számukra a helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="04f28-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="04f28-111">Példák</span><span class="sxs-lookup"><span data-stu-id="04f28-111">EXAMPLES</span></span>

### <span data-ttu-id="04f28-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="04f28-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="04f28-113">Elindítja a helyreállítási terv létrehozása műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="04f28-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="04f28-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04f28-114">PARAMETERS</span></span>

### <span data-ttu-id="04f28-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="04f28-115">-Azure</span></span>
<span data-ttu-id="04f28-116">Váltson paramétert, és adja meg, hogy a helyreállítási terv helyreállítási helye Azure-e.</span><span class="sxs-lookup"><span data-stu-id="04f28-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

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

### <span data-ttu-id="04f28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f28-117">-DefaultProfile</span></span>
<span data-ttu-id="04f28-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04f28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f28-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="04f28-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="04f28-120">Megadja a helyreállítási csomag részét képező replikációs telepítő modellt (klasszikus vagy erőforrás-kezelő) a replikációs védelemmel ellátott elemek között.</span><span class="sxs-lookup"><span data-stu-id="04f28-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="04f28-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04f28-121">-Name</span></span>
<span data-ttu-id="04f28-122">A helyreállítási terv neve.</span><span class="sxs-lookup"><span data-stu-id="04f28-122">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="04f28-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="04f28-123">-Path</span></span>
<span data-ttu-id="04f28-124">A helyreállítási terv definíciója JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="04f28-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="04f28-125">A helyreállítási terv definíciója: a JSON segítségével létrehozhatja a helyreállítási tervet.</span><span class="sxs-lookup"><span data-stu-id="04f28-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="04f28-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="04f28-126">-PrimaryFabric</span></span>
<span data-ttu-id="04f28-127">A helyreállítási csomag részét képező, a replikációs védelemmel ellátott elemek elsődleges ASR-szövetéhez tartozó ASR-szövet objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="04f28-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="04f28-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="04f28-128">-RecoveryFabric</span></span>
<span data-ttu-id="04f28-129">A helyreállítási csomag részét képező replikációs helyreállítási anyaghoz tartozó ASR-szövet objektum.</span><span class="sxs-lookup"><span data-stu-id="04f28-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="04f28-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="04f28-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="04f28-131">A helyreállítási terv első csoportjához hozzáadni kívánt replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="04f28-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="04f28-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04f28-132">-Confirm</span></span>
<span data-ttu-id="04f28-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04f28-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f28-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f28-134">-WhatIf</span></span>
<span data-ttu-id="04f28-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04f28-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04f28-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04f28-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f28-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f28-137">CommonParameters</span></span>
<span data-ttu-id="04f28-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04f28-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f28-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f28-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f28-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04f28-140">INPUTS</span></span>

### <span data-ttu-id="04f28-141">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="04f28-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="04f28-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04f28-142">OUTPUTS</span></span>

### <span data-ttu-id="04f28-143">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="04f28-143">System.Object</span></span>

## <span data-ttu-id="04f28-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04f28-144">NOTES</span></span>

## <span data-ttu-id="04f28-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04f28-145">RELATED LINKS</span></span>

[<span data-ttu-id="04f28-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="04f28-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="04f28-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="04f28-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="04f28-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="04f28-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


