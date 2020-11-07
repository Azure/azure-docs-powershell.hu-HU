---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5627b94f87d69fab6b760bf05f1e22566992048b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679363"
---
# <span data-ttu-id="c67c6-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c67c6-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="c67c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c67c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c67c6-103">Beállítja a helyreállítási tulajdonságokat, például a cél hálózat és a virtuális gép méretét a megadott replikációs védelemmel ellátott elemhez.</span><span class="sxs-lookup"><span data-stu-id="c67c6-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c67c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c67c6-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c67c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c67c6-105">DESCRIPTION</span></span>
<span data-ttu-id="c67c6-106">A **set-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag a replikációs szolgáltatással védett elemek helyreállítási tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="c67c6-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="c67c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c67c6-107">EXAMPLES</span></span>

### <span data-ttu-id="c67c6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c67c6-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="c67c6-109">Elindítja a megadott paraméterekkel a replikációs védelem elem beállításainak frissítését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c67c6-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c67c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c67c6-110">PARAMETERS</span></span>

### <span data-ttu-id="c67c6-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c67c6-111">-InputObject</span></span>
<span data-ttu-id="c67c6-112">A bemeneti objektum a parancsmaghoz: az ASR replikációs szolgáltatással védett elem objektuma, amely megfelel a frissítendő replikációs elemnek.</span><span class="sxs-lookup"><span data-stu-id="c67c6-112">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c67c6-113">-LicenseType</span></span>
<span data-ttu-id="c67c6-114">A Windows Server virtuális gépekhez használt licenc típusának megadása</span><span class="sxs-lookup"><span data-stu-id="c67c6-114">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="c67c6-115">Ha jogosult az Azure Hybrid use haszon (HUB) használatára az áttelepítéshez, és szeretné megállapítani, hogy a HUB beállítás használatban van-e, miközben a védett elem nem szerepel a WindowsServer, adja meg a licenc típusát.</span><span class="sxs-lookup"><span data-stu-id="c67c6-115">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c67c6-116">-Name</span></span>
<span data-ttu-id="c67c6-117">Annak a helyreállítási virtuális gépnek a nevét adja meg, amelyet a feladatátvételkor fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="c67c6-117">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-118">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="c67c6-118">-NicSelectionType</span></span>
<span data-ttu-id="c67c6-119">A hálózati csatolókártya (NIC) tulajdonságát adja meg a felhasználó által megadott vagy alapértelmezés szerint beállítással.</span><span class="sxs-lookup"><span data-stu-id="c67c6-119">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="c67c6-120">A NotSelected megadásával visszatérhet az alapértelmezett értékekhez.</span><span class="sxs-lookup"><span data-stu-id="c67c6-120">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-121">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="c67c6-121">-PrimaryNic</span></span>
<span data-ttu-id="c67c6-122">Annak a virtuális gépnek a NIC-je, amelyhez a parancsmag a helyreállítási hálózat tulajdonságot állítja be.</span><span class="sxs-lookup"><span data-stu-id="c67c6-122">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-123">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="c67c6-123">-RecoveryNetworkId</span></span>
<span data-ttu-id="c67c6-124">Annak az Azure virtuális hálózatnak az AZONOSÍTÓját adja meg, amelyre a védett elemet át kell tenni.</span><span class="sxs-lookup"><span data-stu-id="c67c6-124">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="c67c6-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="c67c6-126">Azt a statikus IP-címet adja meg, amelyet az elsődleges NIC-be kell rendelni a helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="c67c6-126">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-127">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c67c6-127">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="c67c6-128">A helyreállítási Azure virtuális hálózatban annak az alhálózatnak a nevét adja meg, amelyre a védett elemhez tartozó NIC-nek kapcsolódnia kell a feladatátvételhez.</span><span class="sxs-lookup"><span data-stu-id="c67c6-128">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c67c6-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="c67c6-130">Annak az Azure erőforrás-csoportnak az azonosítója, amelynek helyreállítási területén a program a védett elemet helyreállítja a feladatátvétel során.</span><span class="sxs-lookup"><span data-stu-id="c67c6-130">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-131">-Méret</span><span class="sxs-lookup"><span data-stu-id="c67c6-131">-Size</span></span>
<span data-ttu-id="c67c6-132">A helyreállítási virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c67c6-132">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="c67c6-133">Az értéknek az Azure Virtual Machines által támogatott méreteknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c67c6-133">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67c6-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c67c6-134">-Confirm</span></span>
<span data-ttu-id="c67c6-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c67c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c67c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c67c6-136">-WhatIf</span></span>
<span data-ttu-id="c67c6-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c67c6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c67c6-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c67c6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c67c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c67c6-139">CommonParameters</span></span>
<span data-ttu-id="c67c6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c67c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c67c6-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c67c6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c67c6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c67c6-142">INPUTS</span></span>

### <span data-ttu-id="c67c6-143">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c67c6-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c67c6-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c67c6-144">OUTPUTS</span></span>

### <span data-ttu-id="c67c6-145">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c67c6-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c67c6-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c67c6-146">NOTES</span></span>

## <span data-ttu-id="c67c6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c67c6-147">RELATED LINKS</span></span>

[<span data-ttu-id="c67c6-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c67c6-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c67c6-149">Új – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c67c6-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c67c6-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c67c6-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
