---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181462"
---
# <span data-ttu-id="310a2-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="310a2-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="310a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="310a2-102">SYNOPSIS</span></span>
<span data-ttu-id="310a2-103">Beállítja a helyreállítási tulajdonságokat, például a cél hálózat és a virtuális gép méretét a megadott replikációs védelemmel ellátott elemhez.</span><span class="sxs-lookup"><span data-stu-id="310a2-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="310a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="310a2-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="310a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="310a2-105">DESCRIPTION</span></span>
<span data-ttu-id="310a2-106">A **set-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag a replikációs szolgáltatással védett elemek helyreállítási tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="310a2-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="310a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="310a2-107">EXAMPLES</span></span>

### <span data-ttu-id="310a2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="310a2-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="310a2-109">Elindítja a megadott paraméterekkel a replikációs védelemmel ellátott elemek beállításainak frissítését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="310a2-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="310a2-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="310a2-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="310a2-111">Elindítja a replikációs védelemmel ellátott elem hálózati csatoló kártyájának (NIC Reduction) beállításainak frissítését a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="310a2-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="310a2-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="310a2-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="310a2-113">Elindítja a megadott paraméterekkel a replikációs védelemmel ellátott elem (a helyreállított VM-hez használt) beállítások frissítésének műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="310a2-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="310a2-114">4. példa</span><span class="sxs-lookup"><span data-stu-id="310a2-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="310a2-115">Elindítja a megadott paraméterekkel a replikációs védelemmel ellátott elem (a helyreállított VM-hez használt) beállítások frissítésének műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="310a2-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="310a2-116">Példa 5</span><span class="sxs-lookup"><span data-stu-id="310a2-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="310a2-117">Elindítja a replikációs védelemmel ellátott elem frissítésének műveletét (Noc TP), hogy gyorsított hálózatokat engedélyezzen a helyreállítási VM szolgáltatásban (az Azure to Azure katasztrófa-helyreállítás esetén).</span><span class="sxs-lookup"><span data-stu-id="310a2-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="310a2-118">Don t pass-EnableAcceleratedNetworkingOnRecovery a gyorsított hálózat kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="310a2-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="310a2-119">6. példa</span><span class="sxs-lookup"><span data-stu-id="310a2-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="310a2-120">Indítsa el a megadott titkosított replikációs elem frissítési műveletét a feladatátvevő VM-hez tartozó titkosítási adatok használatához.</span><span class="sxs-lookup"><span data-stu-id="310a2-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="310a2-121">7. példa</span><span class="sxs-lookup"><span data-stu-id="310a2-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="310a2-122">A megadott replikációs szolgáltatással védett elem frissítési műveletének megkezdéséhez használja a feladatátvevő VM-hez tartozó megadott közelségi hely csoportot.</span><span class="sxs-lookup"><span data-stu-id="310a2-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="310a2-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="310a2-123">PARAMETERS</span></span>

### <span data-ttu-id="310a2-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="310a2-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="310a2-125">Itt adhatja meg a feladatátvételi és a feladatátvételi NIC-konfiguráció adatait.</span><span class="sxs-lookup"><span data-stu-id="310a2-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310a2-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="310a2-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="310a2-127">Itt adhatja meg a udpated-ra vonatkozó Disk-konfigurációt (Azure to Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="310a2-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="310a2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310a2-128">-DefaultProfile</span></span>
<span data-ttu-id="310a2-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="310a2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="310a2-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="310a2-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="310a2-131">A (Azure Disk Encryption) titkosítással elvégezhető titkosítatlan URL-címet adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="310a2-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="310a2-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="310a2-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="310a2-133">Itt adhatja meg, hogy a rendszer a "titkosítatlan kulcs" kulcsnál (Azure Disk Encryption) a feladatátvétel után használja a helyreállítási VM-et.</span><span class="sxs-lookup"><span data-stu-id="310a2-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="310a2-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="310a2-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="310a2-135">A Disk Resource id to Disk Encryption set ARM azonosító.</span><span class="sxs-lookup"><span data-stu-id="310a2-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310a2-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="310a2-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="310a2-137">A megadott hálózati adaptert adja meg a helyreállítási VM rendszerhez, miután a feladatátvétel a gyorsított hálózatkezelést használja.</span><span class="sxs-lookup"><span data-stu-id="310a2-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310a2-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="310a2-138">-InputObject</span></span>
<span data-ttu-id="310a2-139">A bemeneti objektum a parancsmaghoz: az ASR replikációs szolgáltatással védett elem objektuma, amely megfelel a frissítendő replikációs elemnek.</span><span class="sxs-lookup"><span data-stu-id="310a2-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="310a2-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="310a2-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="310a2-141">A merevlemez-titkosítási kulcs URL-címe (Azure Disk Encryption) a következőre kell használni: Recovery VM a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="310a2-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="310a2-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="310a2-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="310a2-143">A merevlemez-titkosítási kulcs (Azure Disk Encryption) AZONOSÍTÓját adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="310a2-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="310a2-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="310a2-144">-LicenseType</span></span>
<span data-ttu-id="310a2-145">A Windows Server virtuális gépekhez használt licenc típusának megadása</span><span class="sxs-lookup"><span data-stu-id="310a2-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="310a2-146">Ha jogosult az Azure Hybrid use haszon (HUB) használatára az áttelepítéshez, és szeretné megállapítani, hogy a HUB beállítás használatban van-e, miközben a védett elem nem szerepel a WindowsServer, adja meg a licenc típusát.</span><span class="sxs-lookup"><span data-stu-id="310a2-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="310a2-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="310a2-147">-Name</span></span>
<span data-ttu-id="310a2-148">Annak a helyreállítási virtuális gépnek a nevét adja meg, amelyet a feladatátvételkor fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="310a2-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="310a2-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="310a2-149">-NicSelectionType</span></span>
<span data-ttu-id="310a2-150">A hálózati csatolókártya (NIC) tulajdonságát adja meg a felhasználó által megadott vagy alapértelmezés szerint beállítással.</span><span class="sxs-lookup"><span data-stu-id="310a2-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="310a2-151">A NotSelected megadásával visszatérhet az alapértelmezett értékekhez.</span><span class="sxs-lookup"><span data-stu-id="310a2-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="310a2-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="310a2-152">-PrimaryNic</span></span>
<span data-ttu-id="310a2-153">Itt adhatja meg azt a hálózati adaptert, amelyet a feladatátvétel után a recvcovery VM elsődleges hálózati adapterként fog használni.</span><span class="sxs-lookup"><span data-stu-id="310a2-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="310a2-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="310a2-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="310a2-155">A feladatátvétel után a replikációs szolgáltatással védett elemek elérhetőségi beállítása.</span><span class="sxs-lookup"><span data-stu-id="310a2-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="310a2-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="310a2-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="310a2-157">A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="310a2-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="310a2-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="310a2-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="310a2-159">A helyreállítási felhő szolgáltatás erőforrás-azonosítója a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="310a2-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="310a2-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="310a2-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="310a2-161">A helyreállítási hálózati adapterhez társított cél-backend-címkészletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="310a2-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310a2-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="310a2-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="310a2-163">Annak az Azure virtuális hálózatnak az AZONOSÍTÓját adja meg, amelyre a védett elemet át kell tenni.</span><span class="sxs-lookup"><span data-stu-id="310a2-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="310a2-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="310a2-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="310a2-165">Annak a hálózati biztonsági csoportnak az AZONOSÍTÓját adja meg, amely a helyreállítási hálózati kapcsolathoz társítva van.</span><span class="sxs-lookup"><span data-stu-id="310a2-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="310a2-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="310a2-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="310a2-167">Azt a statikus IP-címet adja meg, amelyet az elsődleges NIC-be kell rendelni a helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="310a2-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="310a2-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="310a2-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="310a2-169">A helyreállítási Azure virtuális hálózatban annak az alhálózatnak a nevét adja meg, amelyre a védett elemhez tartozó NIC-nek kapcsolódnia kell a feladatátvételhez.</span><span class="sxs-lookup"><span data-stu-id="310a2-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="310a2-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="310a2-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="310a2-171">A helyreállítási közelségi csoport erőforrás-azonosítóját adja meg a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="310a2-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="310a2-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="310a2-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="310a2-173">A helyreállítási hálózati kapcsolattal társított nyilvános IP-cím erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="310a2-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="310a2-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="310a2-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="310a2-175">Annak az Azure erőforrás-csoportnak az azonosítója, amelynek helyreállítási területén a program a védett elemet helyreállítja a feladatátvétel során.</span><span class="sxs-lookup"><span data-stu-id="310a2-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="310a2-176">-Méret</span><span class="sxs-lookup"><span data-stu-id="310a2-176">-Size</span></span>
<span data-ttu-id="310a2-177">A helyreállítási virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="310a2-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="310a2-178">Az értéknek az Azure Virtual Machines által támogatott méreteknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="310a2-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="310a2-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="310a2-179">-TfoAzureVMName</span></span>
<span data-ttu-id="310a2-180">A teszt feladatátvételi VM-példányának neve.</span><span class="sxs-lookup"><span data-stu-id="310a2-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="310a2-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="310a2-181">-UpdateNic</span></span>
<span data-ttu-id="310a2-182">Annak a virtuális gépnek a NIC-példányát adja meg, amelyre a parancsmag a helyreállítási hálózat tulajdonságot udpated.</span><span class="sxs-lookup"><span data-stu-id="310a2-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="310a2-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="310a2-183">-UseManagedDisk</span></span>
<span data-ttu-id="310a2-184">Annak megadása, hogy a feladatátvételkor létrehozott Azure virtuális gép használható-e a kezelt lemezekhez.</span><span class="sxs-lookup"><span data-stu-id="310a2-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="310a2-185">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="310a2-185">-Confirm</span></span>
<span data-ttu-id="310a2-186">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="310a2-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310a2-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310a2-187">-WhatIf</span></span>
<span data-ttu-id="310a2-188">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="310a2-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="310a2-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="310a2-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310a2-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310a2-190">CommonParameters</span></span>
<span data-ttu-id="310a2-191">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="310a2-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310a2-192">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="310a2-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310a2-193">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="310a2-193">INPUTS</span></span>

### <span data-ttu-id="310a2-194">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="310a2-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="310a2-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="310a2-195">OUTPUTS</span></span>

### <span data-ttu-id="310a2-196">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="310a2-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="310a2-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="310a2-197">NOTES</span></span>

## <span data-ttu-id="310a2-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="310a2-198">RELATED LINKS</span></span>

[<span data-ttu-id="310a2-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="310a2-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="310a2-200">Új – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="310a2-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="310a2-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="310a2-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
