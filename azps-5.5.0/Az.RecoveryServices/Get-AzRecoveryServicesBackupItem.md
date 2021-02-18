---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 8124122b59dcee8a654d52c6f1d9382cb90e2a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206214"
---
# <span data-ttu-id="eb0e3-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="eb0e3-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="eb0e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb0e3-102">SYNOPSIS</span></span>

<span data-ttu-id="eb0e3-103">Egy biztonsági másolatban lévő tárolóból kapja meg az elemeket.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="eb0e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb0e3-104">SYNTAX</span></span>

### <span data-ttu-id="eb0e3-105">GetItemsForContainer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb0e3-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="eb0e3-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="eb0e3-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="eb0e3-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="eb0e3-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

## <span data-ttu-id="eb0e3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb0e3-108">DESCRIPTION</span></span>

<span data-ttu-id="eb0e3-109">A **Get-AzRecoveryServicesBackupItem** parancsmag egy tárolóban lévő védett elemek listáját és az elemek védelmi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="eb0e3-110">Az Azure Recovery Services-tárolókban regisztrált tárolókban egy vagy több védett elem is lehet.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="eb0e3-111">Azure virtuális gépek esetén csak egy biztonságimásolat-elem lehet a virtuális gép tárolóban.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="eb0e3-112">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="eb0e3-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb0e3-113">EXAMPLES</span></span>

### <span data-ttu-id="eb0e3-114">1. példa: Elem lekérte egy biztonsági másolat tárolóból</span><span class="sxs-lookup"><span data-stu-id="eb0e3-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="eb0e3-115">Az első parancs lekérte az AzureVM típusú tárolót, majd a $Container tárolja.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="eb0e3-116">A második parancs a V2VM nevű biztonságimásolat-elemet $Container, majd a $BackupItem tárolja.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="eb0e3-117">2. példa: Azure-fájlmegosztási elem lekérte a FriendlyNametől</span><span class="sxs-lookup"><span data-stu-id="eb0e3-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="eb0e3-118">Az első parancs lekérte az AzureStorage típusú tárolót, majd tárolja azt a $Container változóban.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="eb0e3-119">A második parancs lekérte azt a biztonságimásolat-elemet, amelynek a friendlyName értéke megegyezik a FriendlyName paraméterben megadott értékkel, majd azt a $BackupItem tárolja.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="eb0e3-120">A FriendlyName paraméter használata több Azure-fájlmegosztás visszaadása esetén is okozhatja a visszaadott értékeket.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="eb0e3-121">Ilyen esetben a parancsmagot a -Name paraméter értékének a lekérdezés eredményhalmazában visszaadott Name tulajdonságként $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="eb0e3-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb0e3-122">PARAMETERS</span></span>

### <span data-ttu-id="eb0e3-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="eb0e3-123">-BackupManagementType</span></span>

<span data-ttu-id="eb0e3-124">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-124">The class of resources being protected.</span></span> <span data-ttu-id="eb0e3-125">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="eb0e3-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb0e3-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="eb0e3-126">AzureVM</span></span>
- <span data-ttu-id="eb0e3-127">MAB</span><span class="sxs-lookup"><span data-stu-id="eb0e3-127">MAB</span></span>
- <span data-ttu-id="eb0e3-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="eb0e3-128">AzureStorage</span></span>
- <span data-ttu-id="eb0e3-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="eb0e3-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-130">-Container</span><span class="sxs-lookup"><span data-stu-id="eb0e3-130">-Container</span></span>

<span data-ttu-id="eb0e3-131">Egy tárolóobjektumot ad meg, amelyből a parancsmag biztonsági másolatot készít.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="eb0e3-132">**AzureRmRecoveryServicesBackupContainer** beszerzéséhez használja a **Get-AzRecoveryServicesBackupContainer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0e3-133">-DefaultProfile</span></span>

<span data-ttu-id="eb0e3-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb0e3-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="eb0e3-135">-DeleteState</span></span>
<span data-ttu-id="eb0e3-136">Annak az elemnek a deletestate-ét adja meg, amely a paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="eb0e3-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb0e3-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="eb0e3-137">ToBeDeleted</span></span>
- <span data-ttu-id="eb0e3-138">Nincs törölve</span><span class="sxs-lookup"><span data-stu-id="eb0e3-138">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="eb0e3-139">-FriendlyName</span></span>
<span data-ttu-id="eb0e3-140">A biztonságiolt elem felhasználóbarát neve</span><span class="sxs-lookup"><span data-stu-id="eb0e3-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="eb0e3-141">-Name</span><span class="sxs-lookup"><span data-stu-id="eb0e3-141">-Name</span></span>

<span data-ttu-id="eb0e3-142">A biztonsági másolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-142">Specifies the name of backup item.</span></span> <span data-ttu-id="eb0e3-143">Fájlmegosztás esetén adja meg a védett fájlmegosztás egyedi azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-143">For file share, specify the unique ID of protected file share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="eb0e3-144">-Policy</span></span>

<span data-ttu-id="eb0e3-145">Védelmi házirend objektum.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-145">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="eb0e3-146">-ProtectionState</span></span>

<span data-ttu-id="eb0e3-147">A védelem állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-147">Specifies the state of protection.</span></span>
<span data-ttu-id="eb0e3-148">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="eb0e3-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb0e3-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-149">IRPending.</span></span>
<span data-ttu-id="eb0e3-150">A kezdeti szinkronizálás nem kezdődött el, és még nincs helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="eb0e3-151">Védett.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-151">Protected.</span></span>
<span data-ttu-id="eb0e3-152">A védelem folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-152">Protection is ongoing.</span></span>
- <span data-ttu-id="eb0e3-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-153">ProtectionError.</span></span>
<span data-ttu-id="eb0e3-154">Védelmi hiba történt.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-154">There is a protection error.</span></span>
- <span data-ttu-id="eb0e3-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-155">ProtectionStopped.</span></span>
<span data-ttu-id="eb0e3-156">A védelem le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-156">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="eb0e3-157">-ProtectionStatus</span></span>

<span data-ttu-id="eb0e3-158">A tárolóban található elem általános védelmi állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="eb0e3-159">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="eb0e3-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb0e3-160">Egészséges</span><span class="sxs-lookup"><span data-stu-id="eb0e3-160">Healthy</span></span>
- <span data-ttu-id="eb0e3-161">Nem edalthy</span><span class="sxs-lookup"><span data-stu-id="eb0e3-161">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="eb0e3-162">-VaultId</span></span>

<span data-ttu-id="eb0e3-163">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-163">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="eb0e3-164">-WorkloadType</span></span>

<span data-ttu-id="eb0e3-165">Az erőforrás terheléstípusa.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-165">Workload type of the resource.</span></span> <span data-ttu-id="eb0e3-166">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="eb0e3-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb0e3-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="eb0e3-167">AzureVM</span></span>
- <span data-ttu-id="eb0e3-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="eb0e3-168">AzureFiles</span></span>
- <span data-ttu-id="eb0e3-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="eb0e3-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0e3-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0e3-170">CommonParameters</span></span>
<span data-ttu-id="eb0e3-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb0e3-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0e3-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb0e3-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0e3-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb0e3-173">INPUTS</span></span>

### <span data-ttu-id="eb0e3-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="eb0e3-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="eb0e3-175">System.String</span><span class="sxs-lookup"><span data-stu-id="eb0e3-175">System.String</span></span>

## <span data-ttu-id="eb0e3-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb0e3-176">OUTPUTS</span></span>

### <span data-ttu-id="eb0e3-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="eb0e3-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="eb0e3-178">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb0e3-178">NOTES</span></span>

## <span data-ttu-id="eb0e3-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb0e3-179">RELATED LINKS</span></span>

[<span data-ttu-id="eb0e3-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="eb0e3-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="eb0e3-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="eb0e3-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="eb0e3-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="eb0e3-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="eb0e3-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="eb0e3-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
