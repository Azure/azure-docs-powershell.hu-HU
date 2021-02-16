---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 21c924d02a18ae60f07abd616809358208256039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158547"
---
# <span data-ttu-id="d4dab-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4dab-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="d4dab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4dab-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dab-103">Beállítja a helyreállítási tulajdonságokat, például a célhálózatot és a virtuális gép méretét a megadott replikációs védelem alatt lévő elemhez.</span><span class="sxs-lookup"><span data-stu-id="d4dab-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="d4dab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4dab-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4dab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4dab-105">DESCRIPTION</span></span>
<span data-ttu-id="d4dab-106">A **Set-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag beállítja a replikációval védett elem helyreállítási tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d4dab-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="d4dab-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4dab-107">EXAMPLES</span></span>

### <span data-ttu-id="d4dab-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d4dab-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="d4dab-109">Elindítja a replikációval védett elemek beállításainak frissítését a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d4dab-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d4dab-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4dab-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="d4dab-111">Elindítja a replikációval védett hálózati kártya (NIC-csökkentés) beállításait a megadott paraméterek használatával, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d4dab-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d4dab-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="d4dab-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="d4dab-113">Elindítja a replikációval védett elem elsődleges NIC(a helyreállított vm )beállításainak a megadott paraméterekkel történő frissítését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d4dab-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d4dab-114">4. példa</span><span class="sxs-lookup"><span data-stu-id="d4dab-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="d4dab-115">Elindítja a replikációval védett NIC elem frissítését (a helyreállított vm)beállítások megadott paraméterekkel történő frissítését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d4dab-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d4dab-116">5. példa</span><span class="sxs-lookup"><span data-stu-id="d4dab-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="d4dab-117">Elindítja a replikációval védett elem frissítését, amely során a kijelölt noc tp lehetővé teszi a gyors hálózatépítést a helyreállítási VM-en (azure–Azure-beli katasztrófa-helyreállítás esetén).</span><span class="sxs-lookup"><span data-stu-id="d4dab-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="d4dab-118">Ne adja át az -EnableAcceleratedNetworkingOnRecoveryt a gyorsított hálózatépítés letiltásához.</span><span class="sxs-lookup"><span data-stu-id="d4dab-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="d4dab-119">6. példa</span><span class="sxs-lookup"><span data-stu-id="d4dab-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="d4dab-120">Indítsa el a frissítési műveletet a megadott titkosított replikációval védett elemhez, és használja a megadott titkosítási adatokat a feladatátvételi VM-hez.</span><span class="sxs-lookup"><span data-stu-id="d4dab-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="d4dab-121">7. példa</span><span class="sxs-lookup"><span data-stu-id="d4dab-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="d4dab-122">Indítsa el a frissítési műveletet a megadott replikációval védett elemhez, hogy a megadott közelítési elhelyezési csoportot használja a feladatátvételi VM-hez.</span><span class="sxs-lookup"><span data-stu-id="d4dab-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="d4dab-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4dab-123">PARAMETERS</span></span>

### <span data-ttu-id="d4dab-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4dab-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="d4dab-125">A teszt feladatátvételi és feladatátvételi NIC konfigurációs adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4dab-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="d4dab-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4dab-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="d4dab-127">Azt a lemezkonfigurációt adja meg, amely a felügyelt lemezes vmhez (Azure–Azure DR scenrio) való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="d4dab-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="d4dab-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4dab-128">-DefaultProfile</span></span>
<span data-ttu-id="d4dab-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4dab-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d4dab-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="d4dab-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="d4dab-131">Megadja a lemeztitkosítási titkos URL-címet verzióval (Azure lemeztitkosítás) a helyreállítási VM-hez a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d4dab-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="d4dab-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="d4dab-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="d4dab-133">Megadja azt a lemeztitkosítási titkos kulcs tárolóazonosítóját (Azure lemeztitkosítás), amely a feladatátvétel után helyreállítási VM-ként használható.</span><span class="sxs-lookup"><span data-stu-id="d4dab-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="d4dab-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="d4dab-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="d4dab-135">A lemezerőforrás-azonosító lemeztitkosítási készlet szótára ARM azonosítót.</span><span class="sxs-lookup"><span data-stu-id="d4dab-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="d4dab-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="d4dab-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="d4dab-137">A megadott NIC-et adja meg helyreállítási virtuális gépen, miután a feladatátvétel felgyorsított hálózatépítést használ.</span><span class="sxs-lookup"><span data-stu-id="d4dab-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="d4dab-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4dab-138">-InputObject</span></span>
<span data-ttu-id="d4dab-139">A parancsmag bemeneti objektuma: Az ASR replikációs védett elemobjektuma, amely megfelel a frissíteni kívánt replikációs védett elemnek.</span><span class="sxs-lookup"><span data-stu-id="d4dab-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="d4dab-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="d4dab-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="d4dab-141">Azt a lemeztitkosítási kulcs URL-verzióját (Azure lemeztitkosítás) adja meg, amely helyreállítási VIRTUÁLIS GÉPként használható a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d4dab-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="d4dab-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="d4dab-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="d4dab-143">Azt a lemeztitkosítási kulcskulcsKulcsVault-azonosítót (Azure lemeztitkosítást) ad meg, amely helyreállítási VM-ként használható a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d4dab-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="d4dab-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d4dab-144">-LicenseType</span></span>
<span data-ttu-id="d4dab-145">A Windows Server virtuális gépek licenctípusának kiválasztása.</span><span class="sxs-lookup"><span data-stu-id="d4dab-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="d4dab-146">Ha jogosult az Azure Hybrid Use Benefit (HUB) használatára az áttelepítések során, és szeretné megadni, hogy a HUB beállítása a védett elem esetén a WindowsServer licenctípusra legyen állítva.</span><span class="sxs-lookup"><span data-stu-id="d4dab-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="d4dab-147">-Name</span><span class="sxs-lookup"><span data-stu-id="d4dab-147">-Name</span></span>
<span data-ttu-id="d4dab-148">Megadja annak a helyreállítási virtuális gépnek a nevét, amely feladatátvétel után jön létre.</span><span class="sxs-lookup"><span data-stu-id="d4dab-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="d4dab-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="d4dab-149">-NicSelectionType</span></span>
<span data-ttu-id="d4dab-150">A felhasználó által beállított vagy alapértelmezés szerint beállított hálózati kártyatulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4dab-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="d4dab-151">Megadhatja, hogy a NotSelected visszatér-e az alapértelmezett értékekhez.</span><span class="sxs-lookup"><span data-stu-id="d4dab-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="d4dab-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="d4dab-152">-PrimaryNic</span></span>
<span data-ttu-id="d4dab-153">Megadja azt a NIC-et, amelyet a feladatátvétel után a virtuális gép elsődleges NIC-ként fog használni.</span><span class="sxs-lookup"><span data-stu-id="d4dab-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="d4dab-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d4dab-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="d4dab-155">Replikációs védelem alatt álló elem elérhetőségi beállítása feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d4dab-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="d4dab-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="d4dab-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="d4dab-157">A replikációval védett elem elérhetőségi zónáját adja meg a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d4dab-157">Specifies availability zone for replication protected item after failover.</span></span>

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

### <span data-ttu-id="d4dab-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d4dab-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="d4dab-159">A helyreállítási azure VM rendszerindítási diagnosztikai eszközének tárfiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4dab-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="d4dab-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="d4dab-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="d4dab-161">A helyreállítási felhőszolgáltatás erőforrás-azonosítója, amely feladatátvételt biztosít a virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="d4dab-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="d4dab-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d4dab-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="d4dab-163">Megadja a helyreállítási NIC-hez társítható cél háttércímkészleteket.</span><span class="sxs-lookup"><span data-stu-id="d4dab-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="d4dab-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="d4dab-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="d4dab-165">Annak a virtuális Azure-hálózatnak az azonosítója, amelynek a védett elemét meg kell hibásodni.</span><span class="sxs-lookup"><span data-stu-id="d4dab-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="d4dab-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d4dab-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="d4dab-167">A helyreállítási NIC-hez társítható hálózati biztonsági csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4dab-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="d4dab-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="d4dab-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="d4dab-169">Azt a statikus IP-címet adja meg, amely a helyreállítás során az elsődleges NIC-hez van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="d4dab-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="d4dab-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="d4dab-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="d4dab-171">Annak az alhálózatnak a nevét adja meg a helyreállítási Azure virtuális hálózaton, amelyhez a védett elem ezen NIC-ját feladatátvétel esetén csatlakoztatni kell.</span><span class="sxs-lookup"><span data-stu-id="d4dab-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="d4dab-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="d4dab-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="d4dab-173">A virtuális gép feladatátvétele érdekében a helyreállítási közelség elhelyezésére vonatkozó csoport erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4dab-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="d4dab-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="d4dab-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="d4dab-175">A helyreállítási NIC-hez társítható nyilvános IP-címerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4dab-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="d4dab-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d4dab-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="d4dab-177">Annak az Azure-erőforráscsoportnak az azonosítója abban a helyreállítási régióban, amelyben a védett elem feladatátvétel esetén helyreállítható.</span><span class="sxs-lookup"><span data-stu-id="d4dab-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="d4dab-178">-Size</span><span class="sxs-lookup"><span data-stu-id="d4dab-178">-Size</span></span>
<span data-ttu-id="d4dab-179">A helyreállítási virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4dab-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="d4dab-180">Az értéknek az Azure virtuális gépek által támogatott mérethalmazból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d4dab-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="d4dab-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="d4dab-181">-TfoAzureVMName</span></span>
<span data-ttu-id="d4dab-182">A teszt feladatátvevő virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4dab-182">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="d4dab-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="d4dab-183">-UpdateNic</span></span>
<span data-ttu-id="d4dab-184">Annak a virtuális gépnek a NIC-ét adja meg, amelyhez ez a parancsmag beállítja a helyreállítási hálózati tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d4dab-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="d4dab-185">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d4dab-185">-UseManagedDisk</span></span>
<span data-ttu-id="d4dab-186">Azt adja meg, hogy a feladatátvételre létrehozott Azure virtuális gépnek felügyelt lemezeket kell-e használnia.</span><span class="sxs-lookup"><span data-stu-id="d4dab-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="d4dab-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4dab-187">-Confirm</span></span>
<span data-ttu-id="d4dab-188">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4dab-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4dab-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4dab-189">-WhatIf</span></span>
<span data-ttu-id="d4dab-190">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4dab-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4dab-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4dab-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4dab-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dab-192">CommonParameters</span></span>
<span data-ttu-id="d4dab-193">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4dab-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dab-194">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4dab-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dab-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4dab-195">INPUTS</span></span>

### <span data-ttu-id="d4dab-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4dab-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d4dab-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4dab-197">OUTPUTS</span></span>

### <span data-ttu-id="d4dab-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="d4dab-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4dab-199">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4dab-199">NOTES</span></span>

## <span data-ttu-id="d4dab-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4dab-200">RELATED LINKS</span></span>

[<span data-ttu-id="d4dab-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4dab-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d4dab-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4dab-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d4dab-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4dab-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
