---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 6863c1c8b486784339cf0e1a52cc0793c0cc31f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003142"
---
# <span data-ttu-id="b709b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="b709b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="b709b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b709b-102">SYNOPSIS</span></span>
<span data-ttu-id="b709b-103">Lemezleképezés objektumot hoz létre az Azure virtuális számítógép lemezei replikálása során.</span><span class="sxs-lookup"><span data-stu-id="b709b-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="b709b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b709b-104">SYNTAX</span></span>

### <span data-ttu-id="b709b-105">AzureToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b709b-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b709b-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b709b-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b709b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b709b-107">DESCRIPTION</span></span>
<span data-ttu-id="b709b-108">Létrehoz egy lemezmegfeleltetési objektumot, amely megfeleltet egy Azure virtuális számítógép lemezét a gyorsítótár-tárfióknak és a céltárhelyfióknak (helyreállítási régiónak), amely a lemez replikálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="b709b-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="b709b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b709b-109">EXAMPLES</span></span>

### <span data-ttu-id="b709b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b709b-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="b709b-111">Hozzon létre egy lemezleképezési objektumot az Azure virtuális gépi lemezei replikálása során. Azure–Azure EnableDr- és újravédelem alatt használható.</span><span class="sxs-lookup"><span data-stu-id="b709b-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="b709b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="b709b-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="b709b-113">Hozzon létre egy felügyelt lemezleképezés-objektumot az Azure virtuális gépi lemezei replikálása során. Azure–Azure EnableDr- és újravédelem alatt használható.</span><span class="sxs-lookup"><span data-stu-id="b709b-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="b709b-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="b709b-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="b709b-115">Hozzon létre egy felügyelt lemezleképezés-objektumot egyetlen áttitkosítási beállítással az Azure virtuális számítógép lemezei replikálása esetén. Azure–Azure EnableDr- és újravédelem alatt használható.</span><span class="sxs-lookup"><span data-stu-id="b709b-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="b709b-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="b709b-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="b709b-117">Hozzon létre egy felügyelt lemezleképezési objektumot cél lemeztitkosítási készletazonosítóval, hogy az Azure virtuális számítógép lemezei replikálhatók legyen. Azure–Azure EnableDr- és újravédelem alatt használható.</span><span class="sxs-lookup"><span data-stu-id="b709b-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="b709b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b709b-118">PARAMETERS</span></span>

### <span data-ttu-id="b709b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b709b-119">-DefaultProfile</span></span>
<span data-ttu-id="b709b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b709b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b709b-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="b709b-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="b709b-122">A lemeztitkosítási titkos URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="b709b-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="b709b-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="b709b-124">A lemeztitkosítási kulcs tárolójának ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b709b-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="b709b-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="b709b-125">-DiskId</span></span>
<span data-ttu-id="b709b-126">A felügyelt lemez lemezazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="b709b-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="b709b-127">-FailoverDiskName</span></span>
<span data-ttu-id="b709b-128">A feladatátvétel során létrehozott lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="b709b-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="b709b-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="b709b-130">A kulcstitkosítási URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="b709b-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="b709b-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="b709b-132">A kulcstitkosítási kulcs tárolójának ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b709b-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="b709b-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b709b-133">-LogStorageAccountId</span></span>
<span data-ttu-id="b709b-134">A replikációs naplók tárolásához használt napló- vagy gyorsítótárfiók-azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="b709b-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b709b-135">-ManagedDisk</span></span>
<span data-ttu-id="b709b-136">Azt adja meg, hogy a bevitel a felügyelt lemezhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="b709b-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="b709b-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b709b-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b709b-138">Annak az Azure-tárfióknak az azonosítója, amelybe replikálni kell.</span><span class="sxs-lookup"><span data-stu-id="b709b-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="b709b-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b709b-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="b709b-140">A helyreállítási lemezhez használt Azure lemeztitkosítási készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b709b-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="b709b-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="b709b-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="b709b-142">A replikált felügyelt lemez fióktípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b709b-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="b709b-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="b709b-144">A replikált felügyelt lemez helyreállítási erőforrás-csoportazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="b709b-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="b709b-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="b709b-146">A replikált felügyelt lemez helyreállítási céllemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b709b-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="b709b-147">-TfoDiskName</span></span>
<span data-ttu-id="b709b-148">A teszt feladatátvétele során létrehozott lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b709b-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="b709b-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b709b-149">-VhdUri</span></span>
<span data-ttu-id="b709b-150">Adja meg annak a lemeznek a VHD URI-ját, amely megfelel a megfeleltetésnek.</span><span class="sxs-lookup"><span data-stu-id="b709b-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="b709b-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b709b-151">-Confirm</span></span>
<span data-ttu-id="b709b-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b709b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b709b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b709b-153">-WhatIf</span></span>
<span data-ttu-id="b709b-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b709b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b709b-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b709b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b709b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b709b-156">CommonParameters</span></span>
<span data-ttu-id="b709b-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b709b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b709b-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b709b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b709b-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b709b-159">INPUTS</span></span>

### <span data-ttu-id="b709b-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="b709b-160">None</span></span>

## <span data-ttu-id="b709b-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b709b-161">OUTPUTS</span></span>

### <span data-ttu-id="b709b-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="b709b-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="b709b-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b709b-163">NOTES</span></span>

## <span data-ttu-id="b709b-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b709b-164">RELATED LINKS</span></span>
