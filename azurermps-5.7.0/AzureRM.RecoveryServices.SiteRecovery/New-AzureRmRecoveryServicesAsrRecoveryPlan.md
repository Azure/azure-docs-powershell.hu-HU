---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: e9edfb1654e623b023a075cb462fedfbd9442756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494399"
---
# <span data-ttu-id="45524-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45524-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="45524-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45524-102">SYNOPSIS</span></span>
<span data-ttu-id="45524-103">ASR-helyreállítási csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="45524-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45524-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45524-104">SYNTAX</span></span>

### <span data-ttu-id="45524-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45524-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45524-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="45524-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45524-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="45524-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45524-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="45524-108">DESCRIPTION</span></span>
<span data-ttu-id="45524-109">A **New-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag az Azure webhely-helyreállítási helyreállítási csomagot hoz létre a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="45524-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="45524-110">A helyreállítási terv az alkalmazásba tartozó virtuális gépeket egy egységbe gyűjti, amely lehetővé teszi számukra a helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="45524-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="45524-111">Példák</span><span class="sxs-lookup"><span data-stu-id="45524-111">EXAMPLES</span></span>

### <span data-ttu-id="45524-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45524-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="45524-113">Elindítja a helyreállítási terv létrehozása műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="45524-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="45524-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45524-114">PARAMETERS</span></span>

### <span data-ttu-id="45524-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="45524-115">-Azure</span></span>
<span data-ttu-id="45524-116">Váltson paramétert, és adja meg, hogy a helyreállítási terv helyreállítási helye Azure-e.</span><span class="sxs-lookup"><span data-stu-id="45524-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45524-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45524-117">-Confirm</span></span>
<span data-ttu-id="45524-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45524-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45524-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45524-119">-DefaultProfile</span></span>
<span data-ttu-id="45524-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45524-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="45524-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="45524-121">-FailoverDeploymentModel</span></span>
<span data-ttu-id="45524-122">Megadja a helyreállítási csomag részét képező replikációs telepítő modellt (klasszikus vagy erőforrás-kezelő) a replikációs védelemmel ellátott elemek között.</span><span class="sxs-lookup"><span data-stu-id="45524-122">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45524-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45524-123">-Name</span></span>
<span data-ttu-id="45524-124">A helyreállítási terv neve.</span><span class="sxs-lookup"><span data-stu-id="45524-124">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45524-125">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="45524-125">-Path</span></span>
<span data-ttu-id="45524-126">A helyreállítási terv definíciója JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45524-126">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="45524-127">A helyreállítási terv definíciója: a JSON segítségével létrehozhatja a helyreállítási tervet.</span><span class="sxs-lookup"><span data-stu-id="45524-127">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45524-128">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="45524-128">-PrimaryFabric</span></span>
<span data-ttu-id="45524-129">A helyreállítási csomag részét képező, a replikációs védelemmel ellátott elemek elsődleges ASR-szövetéhez tartozó ASR-szövet objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="45524-129">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45524-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="45524-130">-RecoveryFabric</span></span>
<span data-ttu-id="45524-131">A helyreállítási csomag részét képező replikációs helyreállítási anyaghoz tartozó ASR-szövet objektum.</span><span class="sxs-lookup"><span data-stu-id="45524-131">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45524-132">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="45524-132">-ReplicationProtectedItem</span></span>
<span data-ttu-id="45524-133">A helyreállítási terv első csoportjához hozzáadni kívánt replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="45524-133">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45524-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45524-134">-WhatIf</span></span>
<span data-ttu-id="45524-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45524-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45524-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45524-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45524-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45524-137">CommonParameters</span></span>
<span data-ttu-id="45524-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45524-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45524-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45524-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45524-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45524-140">INPUTS</span></span>

### <span data-ttu-id="45524-141">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="45524-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="45524-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45524-142">OUTPUTS</span></span>

### <span data-ttu-id="45524-143">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="45524-143">System.Object</span></span>

## <span data-ttu-id="45524-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45524-144">NOTES</span></span>

## <span data-ttu-id="45524-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45524-145">RELATED LINKS</span></span>

[<span data-ttu-id="45524-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45524-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="45524-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45524-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="45524-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45524-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


