---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184702"
---
# <span data-ttu-id="8d84c-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8d84c-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8d84c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d84c-102">SYNOPSIS</span></span>

<span data-ttu-id="8d84c-103">Beolvassa az elemeket egy tárolóból a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="8d84c-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="8d84c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d84c-104">SYNTAX</span></span>

### <span data-ttu-id="8d84c-105">GetItemsForContainer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d84c-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d84c-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="8d84c-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d84c-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="8d84c-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d84c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d84c-108">DESCRIPTION</span></span>

<span data-ttu-id="8d84c-109">A **Get-AzRecoveryServicesBackupItem** parancsmag egy tárolóban lévő védett elemek listáját és az elemek védettségi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8d84c-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="8d84c-110">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="8d84c-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="8d84c-111">Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy biztonságimásolat-elem lehet.</span><span class="sxs-lookup"><span data-stu-id="8d84c-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="8d84c-112">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="8d84c-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="8d84c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8d84c-113">EXAMPLES</span></span>

### <span data-ttu-id="8d84c-114">Példa 1: elem beszerzése biztonsági tárolóból</span><span class="sxs-lookup"><span data-stu-id="8d84c-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="8d84c-115">Az első parancs beolvassa a AzureVM típusú dobozt, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8d84c-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8d84c-116">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Container, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8d84c-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="8d84c-117">2. példa: Azure-fájlmegosztás elemének beszerzése a típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="8d84c-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="8d84c-118">Az első parancs beolvassa a AzureStorage típusú dobozt, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8d84c-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8d84c-119">A második parancs azt a biztonsági másolatot kapja, amelynek a típusú megjelenített megegyezik a típusú megjelenített paraméterben átadott értékkel, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8d84c-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8d84c-120">A típusú megjelenített paraméter használata több Azure-fájlmegosztás visszaadásához vezethet.</span><span class="sxs-lookup"><span data-stu-id="8d84c-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="8d84c-121">Az ilyen esetekben a parancsmagot úgy kell végrehajtania, hogy a Name (név) paramétert átviszi a név tulajdonságra az $BackupItem eredményhalmazban.</span><span class="sxs-lookup"><span data-stu-id="8d84c-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="8d84c-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d84c-122">PARAMETERS</span></span>

### <span data-ttu-id="8d84c-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8d84c-123">-BackupManagementType</span></span>

<span data-ttu-id="8d84c-124">A védelemmel ellátott erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="8d84c-124">The class of resources being protected.</span></span> <span data-ttu-id="8d84c-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d84c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d84c-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="8d84c-126">AzureVM</span></span>
- <span data-ttu-id="8d84c-127">Mohácsi</span><span class="sxs-lookup"><span data-stu-id="8d84c-127">MAB</span></span>
- <span data-ttu-id="8d84c-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="8d84c-128">AzureStorage</span></span>
- <span data-ttu-id="8d84c-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="8d84c-129">AzureWorkload</span></span>

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

### <span data-ttu-id="8d84c-130">-Container</span><span class="sxs-lookup"><span data-stu-id="8d84c-130">-Container</span></span>

<span data-ttu-id="8d84c-131">Azt a tároló objektumot adja meg, amelyből a parancsmag biztonsági mentési elemeket kap.</span><span class="sxs-lookup"><span data-stu-id="8d84c-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="8d84c-132">**AzureRmRecoveryServicesBackupContainer** beszerzéséhez használja a **Get-AzRecoveryServicesBackupContainer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8d84c-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="8d84c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d84c-133">-DefaultProfile</span></span>

<span data-ttu-id="8d84c-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d84c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d84c-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="8d84c-135">-DeleteState</span></span>
<span data-ttu-id="8d84c-136">Az elem deletestate adja meg, hogy a paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d84c-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d84c-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="8d84c-137">ToBeDeleted</span></span>
- <span data-ttu-id="8d84c-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="8d84c-138">NotDeleted</span></span>

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

### <span data-ttu-id="8d84c-139">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="8d84c-139">-FriendlyName</span></span>
<span data-ttu-id="8d84c-140">A mentett elem típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="8d84c-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="8d84c-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d84c-141">-Name</span></span>

<span data-ttu-id="8d84c-142">A biztonságimásolat-elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d84c-142">Specifies the name of backup item.</span></span> <span data-ttu-id="8d84c-143">Fájlmegosztás esetén adja meg a védett fájlmegosztás egyedi AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="8d84c-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="8d84c-144">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8d84c-144">-Policy</span></span>

<span data-ttu-id="8d84c-145">Protection Policy objektum.</span><span class="sxs-lookup"><span data-stu-id="8d84c-145">Protection policy object.</span></span>

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

### <span data-ttu-id="8d84c-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="8d84c-146">-ProtectionState</span></span>

<span data-ttu-id="8d84c-147">A védelmi államot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d84c-147">Specifies the state of protection.</span></span>
<span data-ttu-id="8d84c-148">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d84c-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d84c-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="8d84c-149">IRPending.</span></span>
<span data-ttu-id="8d84c-150">A kezdeti szinkronizálás még nem kezdődött el, és még nincs helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="8d84c-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="8d84c-151">Védett.</span><span class="sxs-lookup"><span data-stu-id="8d84c-151">Protected.</span></span>
<span data-ttu-id="8d84c-152">A védelem folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="8d84c-152">Protection is ongoing.</span></span>
- <span data-ttu-id="8d84c-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="8d84c-153">ProtectionError.</span></span>
<span data-ttu-id="8d84c-154">Van egy védelmi hiba.</span><span class="sxs-lookup"><span data-stu-id="8d84c-154">There is a protection error.</span></span>
- <span data-ttu-id="8d84c-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="8d84c-155">ProtectionStopped.</span></span>
<span data-ttu-id="8d84c-156">A védelem le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="8d84c-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="8d84c-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="8d84c-157">-ProtectionStatus</span></span>

<span data-ttu-id="8d84c-158">A tároló elemeinek általános védelmi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d84c-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="8d84c-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d84c-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d84c-160">Egészséges</span><span class="sxs-lookup"><span data-stu-id="8d84c-160">Healthy</span></span>
- <span data-ttu-id="8d84c-161">Egészségtelen</span><span class="sxs-lookup"><span data-stu-id="8d84c-161">Unhealthy</span></span>

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

### <span data-ttu-id="8d84c-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8d84c-162">-VaultId</span></span>

<span data-ttu-id="8d84c-163">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="8d84c-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8d84c-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="8d84c-164">-WorkloadType</span></span>

<span data-ttu-id="8d84c-165">Az erőforrás terhelési típusa.</span><span class="sxs-lookup"><span data-stu-id="8d84c-165">Workload type of the resource.</span></span> <span data-ttu-id="8d84c-166">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d84c-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d84c-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="8d84c-167">AzureVM</span></span>
- <span data-ttu-id="8d84c-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="8d84c-168">AzureFiles</span></span>
- <span data-ttu-id="8d84c-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="8d84c-169">MSSQL</span></span>

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

### <span data-ttu-id="8d84c-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d84c-170">CommonParameters</span></span>
<span data-ttu-id="8d84c-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d84c-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d84c-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d84c-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d84c-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d84c-173">INPUTS</span></span>

### <span data-ttu-id="8d84c-174">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="8d84c-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="8d84c-175">System. String</span><span class="sxs-lookup"><span data-stu-id="8d84c-175">System.String</span></span>

## <span data-ttu-id="8d84c-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d84c-176">OUTPUTS</span></span>

### <span data-ttu-id="8d84c-177">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="8d84c-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="8d84c-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d84c-178">NOTES</span></span>

## <span data-ttu-id="8d84c-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d84c-179">RELATED LINKS</span></span>

[<span data-ttu-id="8d84c-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8d84c-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8d84c-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8d84c-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="8d84c-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8d84c-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="8d84c-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8d84c-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
