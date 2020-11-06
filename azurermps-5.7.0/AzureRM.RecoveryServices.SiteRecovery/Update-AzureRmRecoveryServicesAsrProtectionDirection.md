---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 13d1829326695e2860caf99bf002dcf5da31caac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493035"
---
# <span data-ttu-id="e88e7-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="e88e7-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="e88e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e88e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e88e7-103">Frissíti a megadott replikációs védett elem vagy helyreállítási terv replikációs irányát.</span><span class="sxs-lookup"><span data-stu-id="e88e7-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="e88e7-104">A replikált elem vagy helyreállítási terv ismételt védelméhez/visszavonásához használható.</span><span class="sxs-lookup"><span data-stu-id="e88e7-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e88e7-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e88e7-105">SYNTAX</span></span>

### <span data-ttu-id="e88e7-106">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e88e7-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88e7-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="e88e7-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e88e7-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e88e7-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88e7-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="e88e7-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88e7-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e88e7-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88e7-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e88e7-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88e7-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e88e7-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88e7-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e88e7-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88e7-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="e88e7-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88e7-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="e88e7-115">DESCRIPTION</span></span>
<span data-ttu-id="e88e7-116">Az **Update-AzureRmRecoveryServicesAsrProtectionDirection** parancsmag a megadott Azure-webhely helyreállítási objektumának replikációs irányát frissíti a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="e88e7-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="e88e7-117">Példák</span><span class="sxs-lookup"><span data-stu-id="e88e7-117">EXAMPLES</span></span>

### <span data-ttu-id="e88e7-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e88e7-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="e88e7-119">Indítsa el a megadott helyreállítási csomag frissítési irányát, és a művelet nyomon követéséhez használt ASR-objektum értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e88e7-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="e88e7-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="e88e7-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="e88e7-121">A megfelelő replikációs védelemmel ellátott elem frissítési irányának indítása a tároló Azure-területen, a tároló-tárolók megfeleltetése és a gyorsítótár-tároló használata (a VM-ben).</span><span class="sxs-lookup"><span data-stu-id="e88e7-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="e88e7-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="e88e7-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="e88e7-123">A megfelelő replikációs védett elem frissítési irányának indítása a tároló Azure régióban, a védett tárolók megfeleltetése és a lemezkvóta-konfiguráció megadása által meghatározva.</span><span class="sxs-lookup"><span data-stu-id="e88e7-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="e88e7-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e88e7-124">PARAMETERS</span></span>

### <span data-ttu-id="e88e7-125">-Fiók</span><span class="sxs-lookup"><span data-stu-id="e88e7-125">-Account</span></span>
<span data-ttu-id="e88e7-126">A Futtatás mint fiók, amellyel szükség esetén lenyomhatja a mobil szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e88e7-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="e88e7-127">Az ASR-anyagban a Run as (futtatási) fiókból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e88e7-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e88e7-128">-AzureToAzure</span></span>
<span data-ttu-id="e88e7-129">A kapcsoló paraméter azt adja meg, hogy a replikálási irány frissítve legyenek a replikált Azure virtuális gépek között két Azure régió között.</span><span class="sxs-lookup"><span data-stu-id="e88e7-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="e88e7-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="e88e7-131">A replikálni kívánt virtuálisgép-lemezek listáját adja meg, valamint a gyorsítótár-tárolási fiókot és a helyreállítási tárterületet, amelyet a lemez replikálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="e88e7-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="e88e7-132">-AzureToVMware</span></span>
<span data-ttu-id="e88e7-133">Replikációs irány frissítése az Azure-től a VMware-ig</span><span class="sxs-lookup"><span data-stu-id="e88e7-133">Update replication direction from Azure to Vmware.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e88e7-134">-Confirm</span></span>
<span data-ttu-id="e88e7-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e88e7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88e7-136">-Adattár</span><span class="sxs-lookup"><span data-stu-id="e88e7-136">-DataStore</span></span>
<span data-ttu-id="e88e7-137">A vmdisk használt VMware adattár.</span><span class="sxs-lookup"><span data-stu-id="e88e7-137">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88e7-138">-DefaultProfile</span></span>
<span data-ttu-id="e88e7-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e88e7-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e88e7-140">-Irány</span><span class="sxs-lookup"><span data-stu-id="e88e7-140">-Direction</span></span>
<span data-ttu-id="e88e7-141">Megadja, hogy milyen irányt kell használni a frissítési művelethez a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="e88e7-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="e88e7-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e88e7-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e88e7-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e88e7-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="e88e7-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e88e7-144">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-145">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="e88e7-145">-HyperVToAzure</span></span>
<span data-ttu-id="e88e7-146">A Hyper-V virtuális gép újravédelme a visszaállás után.</span><span class="sxs-lookup"><span data-stu-id="e88e7-146">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-147">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e88e7-147">-LogStorageAccountId</span></span>
<span data-ttu-id="e88e7-148">Megadja a tárolási fiók AZONOSÍTÓját a VMs-alapú replikációs napló tárolásához.</span><span class="sxs-lookup"><span data-stu-id="e88e7-148">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-149">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="e88e7-149">-MasterTarget</span></span>
<span data-ttu-id="e88e7-150">A fő célkiszolgáló adatai</span><span class="sxs-lookup"><span data-stu-id="e88e7-150">Master Target Server Details.</span></span>

```yaml
Type: ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="e88e7-151">-ProcessServer</span></span>
<span data-ttu-id="e88e7-152">A replikációhoz használandó folyamat kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="e88e7-152">Process Server to be used for replication.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-153">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e88e7-153">-ProtectionContainerMapping</span></span>
<span data-ttu-id="e88e7-154">A replikációhoz használni kívánt védelmi containerMapping.</span><span class="sxs-lookup"><span data-stu-id="e88e7-154">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-155">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="e88e7-155">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="e88e7-156">Az elérhetőségi készlet, amelyet a virtuális gép a feladatátvételkor hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e88e7-156">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-157">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e88e7-157">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e88e7-158">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e88e7-158">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="e88e7-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="e88e7-160">A helyreállítási felhő szolgáltatás erőforrás-azonosítója a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="e88e7-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e88e7-161">-RecoveryPlan</span></span>
<span data-ttu-id="e88e7-162">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e88e7-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e88e7-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e88e7-164">Helyreállítási resourceGroup-azonosító a védett VM-hez.</span><span class="sxs-lookup"><span data-stu-id="e88e7-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e88e7-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e88e7-166">Egy ASR-replikációs védelemmel ellátott elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="e88e7-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="e88e7-167">-RetentionVolume</span></span>
<span data-ttu-id="e88e7-168">Az adatmegőrzési mennyiség a fő célként használt kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e88e7-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-169">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e88e7-169">-VMwareToAzure</span></span>
<span data-ttu-id="e88e7-170">Frissítse a replikációs irányt a VMware-től az Azure-ig.</span><span class="sxs-lookup"><span data-stu-id="e88e7-170">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="e88e7-171">-VmmToVmm</span></span>
<span data-ttu-id="e88e7-172">A replikáció irányának frissítése nem sikerült a Hyper-V virtuális gépén, amely két VMM felügyelt Hyper-V-webhelytől védett.</span><span class="sxs-lookup"><span data-stu-id="e88e7-172">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88e7-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88e7-173">-WhatIf</span></span>
<span data-ttu-id="e88e7-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e88e7-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e88e7-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e88e7-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88e7-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88e7-176">CommonParameters</span></span>
<span data-ttu-id="e88e7-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e88e7-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88e7-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88e7-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88e7-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e88e7-179">INPUTS</span></span>

### <span data-ttu-id="e88e7-180">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e88e7-180">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="e88e7-181">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e88e7-181">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e88e7-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e88e7-182">OUTPUTS</span></span>

### <span data-ttu-id="e88e7-183">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e88e7-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e88e7-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e88e7-184">NOTES</span></span>

## <span data-ttu-id="e88e7-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e88e7-185">RELATED LINKS</span></span>
