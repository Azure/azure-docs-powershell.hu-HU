---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 11598952da67d7f3b3ec94f6c64b71c80bbad12c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839033"
---
# <span data-ttu-id="7bdb3-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdb3-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7bdb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdb3-103">Beállítja a helyreállítási tulajdonságokat, például a cél hálózat és a virtuális gép méretét a megadott replikációs védelemmel ellátott elemhez.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="7bdb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bdb3-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryCloudServiceId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-RecoveryAvailabilitySet <String>]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bdb3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bdb3-105">DESCRIPTION</span></span>
<span data-ttu-id="7bdb3-106">A **set-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag a replikációs szolgáltatással védett elemek helyreállítási tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="7bdb3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7bdb3-107">EXAMPLES</span></span>

### <span data-ttu-id="7bdb3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7bdb3-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="7bdb3-109">Elindítja a megadott paraméterekkel a replikációs védelem elem beállításainak frissítését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7bdb3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bdb3-110">PARAMETERS</span></span>

### <span data-ttu-id="7bdb3-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bdb3-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="7bdb3-112">{{Fill AzureToAzureUpdateReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="7bdb3-112">{{Fill AzureToAzureUpdateReplicationConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdb3-113">-DefaultProfile</span></span>
<span data-ttu-id="7bdb3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7bdb3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bdb3-115">-InputObject</span></span>
<span data-ttu-id="7bdb3-116">A bemeneti objektum a parancsmaghoz: az ASR replikációs szolgáltatással védett elem objektuma, amely megfelel a frissítendő replikációs elemnek.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7bdb3-117">-LicenseType</span></span>
<span data-ttu-id="7bdb3-118">A Windows Server virtuális gépekhez használt licenc típusának megadása</span><span class="sxs-lookup"><span data-stu-id="7bdb3-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="7bdb3-119">Ha jogosult az Azure Hybrid use haszon (HUB) használatára az áttelepítéshez, és szeretné megállapítani, hogy a HUB beállítás használatban van-e, miközben a védett elem nem szerepel a WindowsServer, adja meg a licenc típusát.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7bdb3-120">-Name</span></span>
<span data-ttu-id="7bdb3-121">Annak a helyreállítási virtuális gépnek a nevét adja meg, amelyet a feladatátvételkor fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="7bdb3-122">-NicSelectionType</span></span>
<span data-ttu-id="7bdb3-123">A hálózati csatolókártya (NIC) tulajdonságát adja meg a felhasználó által megadott vagy alapértelmezés szerint beállítással.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="7bdb3-124">A NotSelected megadásával visszatérhet az alapértelmezett értékekhez.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="7bdb3-125">-PrimaryNic</span></span>
<span data-ttu-id="7bdb3-126">Annak a virtuális gépnek a NIC-je, amelyhez a parancsmag a helyreállítási hálózat tulajdonságot állítja be.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7bdb3-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="7bdb3-128">A feladatátvétel után a replikációs szolgáltatással védett elemek elérhetőségi beállítása.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-128">Availability set for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7bdb3-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="7bdb3-130">A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="7bdb3-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="7bdb3-132">A helyreállítási felhő szolgáltatás erőforrás-azonosítója a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="7bdb3-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="7bdb3-134">Annak az Azure virtuális hálózatnak az AZONOSÍTÓját adja meg, amelyre a védett elemet át kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="7bdb3-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="7bdb3-136">Azt a statikus IP-címet adja meg, amelyet az elsődleges NIC-be kell rendelni a helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="7bdb3-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="7bdb3-138">A helyreállítási Azure virtuális hálózatban annak az alhálózatnak a nevét adja meg, amelyre a védett elemhez tartozó NIC-nek kapcsolódnia kell a feladatátvételhez.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="7bdb3-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="7bdb3-140">Annak az Azure erőforrás-csoportnak az azonosítója, amelynek helyreállítási területén a program a védett elemet helyreállítja a feladatátvétel során.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-141">-Méret</span><span class="sxs-lookup"><span data-stu-id="7bdb3-141">-Size</span></span>
<span data-ttu-id="7bdb3-142">A helyreállítási virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="7bdb3-143">Az értéknek az Azure Virtual Machines által támogatott méreteknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7bdb3-144">-UseManagedDisk</span></span>
<span data-ttu-id="7bdb3-145">Annak megadása, hogy a feladatátvételkor létrehozott Azure virtuális gép használható-e a kezelt lemezekhez.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdb3-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7bdb3-146">-Confirm</span></span>
<span data-ttu-id="7bdb3-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bdb3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bdb3-148">-WhatIf</span></span>
<span data-ttu-id="7bdb3-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bdb3-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bdb3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bdb3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdb3-151">CommonParameters</span></span>
<span data-ttu-id="7bdb3-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bdb3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdb3-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bdb3-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdb3-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bdb3-154">INPUTS</span></span>

### <span data-ttu-id="7bdb3-155">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdb3-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7bdb3-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bdb3-156">OUTPUTS</span></span>

### <span data-ttu-id="7bdb3-157">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7bdb3-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7bdb3-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bdb3-158">NOTES</span></span>

## <span data-ttu-id="7bdb3-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bdb3-159">RELATED LINKS</span></span>

[<span data-ttu-id="7bdb3-160">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdb3-160">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7bdb3-161">Új – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdb3-161">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7bdb3-162">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdb3-162">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
