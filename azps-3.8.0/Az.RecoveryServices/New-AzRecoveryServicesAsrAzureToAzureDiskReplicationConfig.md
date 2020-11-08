---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: b5d369a4f67888d6b7035e81d3462e10586ca3ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014703"
---
# <span data-ttu-id="8b7b5-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="8b7b5-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="8b7b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7b5-103">Létrehoz egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="8b7b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b7b5-104">SYNTAX</span></span>

### <span data-ttu-id="8b7b5-105">AzureToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b7b5-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b7b5-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8b7b5-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b7b5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b7b5-107">DESCRIPTION</span></span>
<span data-ttu-id="8b7b5-108">Létrehoz egy olyan lemezkezelő-objektumot, amely egy Azure Virtual Machine-merevlemezt rendel a gyorsítótár-tároló fiókhoz és a TARGET Storage (helyreállítási régió) fiókhoz, amelyet a lemez replikálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="8b7b5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8b7b5-109">EXAMPLES</span></span>

### <span data-ttu-id="8b7b5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8b7b5-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="8b7b5-111">Létrehozhat egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához. Az Azure-ban az Azure EnableD és az újravédelemi művelet során használható.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="8b7b5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8b7b5-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="8b7b5-113">Felügyelt lemezkezelő objektum létrehozása a replikálni kívánt Azure Virtual Machine-lemezekhez. Az Azure-ban az Azure EnableD és az újravédelemi művelet során használható.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="8b7b5-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="8b7b5-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="8b7b5-115">Felügyelt lemezkezelő objektum létrehozása az Azure Virtual Machine-lemezek replikálására szolgáló titkosítási beállításokkal Az Azure-ban az Azure EnableD és az újravédelemi művelet során használható.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="8b7b5-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="8b7b5-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="8b7b5-117">Felügyelt lemezkezelő objektum létrehozása a céllemez-titkosítási készlet azonosítóval az Azure Virtual Machine-lemezek replikálásához. Az Azure-ban az Azure EnableD és az újravédelemi művelet során használható.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="8b7b5-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b7b5-118">PARAMETERS</span></span>

### <span data-ttu-id="8b7b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7b5-119">-DefaultProfile</span></span>
<span data-ttu-id="8b7b5-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b7b5-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="8b7b5-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="8b7b5-122">A Disk Encryption Secret URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8b7b5-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="8b7b5-124">A Disk Encryption Key Vault-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-125">-Csúszásgátló</span><span class="sxs-lookup"><span data-stu-id="8b7b5-125">-DiskId</span></span>
<span data-ttu-id="8b7b5-126">A felügyelt lemez lemezvezérlő-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="8b7b5-127">-FailoverDiskName</span></span>
<span data-ttu-id="8b7b5-128">A feladatátvétel során létrehozott lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8b7b5-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8b7b5-130">A kulcs titkosítási URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8b7b5-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="8b7b5-132">A kulcs-titkosítási kulcs Vault-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8b7b5-133">-LogStorageAccountId</span></span>
<span data-ttu-id="8b7b5-134">A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8b7b5-135">-ManagedDisk</span></span>
<span data-ttu-id="8b7b5-136">Itt adhatja meg, hogy a rendszer a kezelt lemez bemenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8b7b5-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8b7b5-138">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8b7b5-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="8b7b5-140">A helyreállítási lemezekhez használt Azure Disk Encryption set AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="8b7b5-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="8b7b5-142">A replikált távtárolású lemez fiókjának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, Standard_SSD

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8b7b5-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8b7b5-144">A replikált távtárolású lemez helyreállítási erőforráscsoport-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="8b7b5-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="8b7b5-146">A replikált távtárolású lemez helyreállítási célhelyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, Standard_SSD

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="8b7b5-147">-TfoDiskName</span></span>
<span data-ttu-id="8b7b5-148">A teszt-feladatátvétel során létrehozott lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="8b7b5-149">-VhdUri</span></span>
<span data-ttu-id="8b7b5-150">Adja meg annak a lemeznek a VHD-URI-jét, amelyre a megfeleltetés megfelel.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7b5-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b7b5-151">-Confirm</span></span>
<span data-ttu-id="8b7b5-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b7b5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7b5-153">-WhatIf</span></span>
<span data-ttu-id="8b7b5-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b7b5-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b7b5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7b5-156">CommonParameters</span></span>
<span data-ttu-id="8b7b5-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b7b5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7b5-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b7b5-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7b5-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b7b5-159">INPUTS</span></span>

### <span data-ttu-id="8b7b5-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="8b7b5-160">None</span></span>

## <span data-ttu-id="8b7b5-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b7b5-161">OUTPUTS</span></span>

### <span data-ttu-id="8b7b5-162">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="8b7b5-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="8b7b5-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b7b5-163">NOTES</span></span>

## <span data-ttu-id="8b7b5-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b7b5-164">RELATED LINKS</span></span>
