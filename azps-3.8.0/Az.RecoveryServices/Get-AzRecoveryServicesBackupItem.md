---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010890"
---
# <span data-ttu-id="cbdf8-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cbdf8-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="cbdf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbdf8-102">SYNOPSIS</span></span>

<span data-ttu-id="cbdf8-103">Beolvassa az elemeket egy tárolóból a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="cbdf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbdf8-104">SYNTAX</span></span>

### <span data-ttu-id="cbdf8-105">GetItemsForContainer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbdf8-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbdf8-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="cbdf8-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbdf8-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="cbdf8-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbdf8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbdf8-108">DESCRIPTION</span></span>

<span data-ttu-id="cbdf8-109">A **Get-AzRecoveryServicesBackupItem** parancsmag a tárolóban lévő elemeket, illetve az Azure biztonsági másolatban szereplő elemeket, valamint az elemek védelmi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="cbdf8-110">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="cbdf8-111">Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy biztonságimásolat-elem lehet.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="cbdf8-112">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="cbdf8-113">Példák</span><span class="sxs-lookup"><span data-stu-id="cbdf8-113">EXAMPLES</span></span>

### <span data-ttu-id="cbdf8-114">Példa 1: elem beszerzése biztonsági tárolóból</span><span class="sxs-lookup"><span data-stu-id="cbdf8-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="cbdf8-115">Az első parancs beolvassa a AzureVM típusú dobozt, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="cbdf8-116">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Container, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="cbdf8-117">2. példa: Azure-fájlmegosztás elemének beszerzése a típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="cbdf8-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="cbdf8-118">Az első parancs beolvassa a AzureStorage típusú dobozt, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="cbdf8-119">A második parancs azt a biztonsági másolatot kapja, amelynek a típusú megjelenített megegyezik a típusú megjelenített paraméterben átadott értékkel, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="cbdf8-120">A típusú megjelenített paraméter használata több Azure-fájlmegosztás visszaadásához vezethet.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="cbdf8-121">Ebben az esetben a name tulajdonságot $BackupItem változóban a Name tulajdonság értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="cbdf8-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbdf8-122">PARAMETERS</span></span>

### <span data-ttu-id="cbdf8-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="cbdf8-123">-BackupManagementType</span></span>

<span data-ttu-id="cbdf8-124">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="cbdf8-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbdf8-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbdf8-126">AzureVM</span></span>
- <span data-ttu-id="cbdf8-127">MARS</span><span class="sxs-lookup"><span data-stu-id="cbdf8-127">MARS</span></span>
- <span data-ttu-id="cbdf8-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="cbdf8-128">SCDPM</span></span>
- <span data-ttu-id="cbdf8-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="cbdf8-129">AzureBackupServer</span></span>
- <span data-ttu-id="cbdf8-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="cbdf8-130">AzureSQL</span></span>
- <span data-ttu-id="cbdf8-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="cbdf8-131">AzureStorage</span></span>
- <span data-ttu-id="cbdf8-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="cbdf8-132">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdf8-133">-Container</span><span class="sxs-lookup"><span data-stu-id="cbdf8-133">-Container</span></span>

<span data-ttu-id="cbdf8-134">Azt a tároló objektumot adja meg, amelyből a parancsmag biztonsági mentési elemeket kap.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="cbdf8-135">**AzureRmRecoveryServicesBackupContainer** beszerzéséhez használja a **Get-AzRecoveryServicesBackupContainer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="cbdf8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdf8-136">-DefaultProfile</span></span>

<span data-ttu-id="cbdf8-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbdf8-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="cbdf8-138">-DeleteState</span></span>
<span data-ttu-id="cbdf8-139">Az elem deletestate adja meg, hogy a paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbdf8-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="cbdf8-140">ToBeDeleted</span></span>
- <span data-ttu-id="cbdf8-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="cbdf8-141">NotDeleted</span></span>

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

### <span data-ttu-id="cbdf8-142">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="cbdf8-142">-FriendlyName</span></span>
<span data-ttu-id="cbdf8-143">A mentett elem típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="cbdf8-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="cbdf8-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbdf8-144">-Name</span></span>

<span data-ttu-id="cbdf8-145">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="cbdf8-146">-Házirend</span><span class="sxs-lookup"><span data-stu-id="cbdf8-146">-Policy</span></span>

<span data-ttu-id="cbdf8-147">Protection Policy objektum.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-147">Protection policy object.</span></span>

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

### <span data-ttu-id="cbdf8-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="cbdf8-148">-ProtectionState</span></span>

<span data-ttu-id="cbdf8-149">A védelmi államot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-149">Specifies the state of protection.</span></span>
<span data-ttu-id="cbdf8-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbdf8-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-151">IRPending.</span></span>
<span data-ttu-id="cbdf8-152">A kezdeti szinkronizálás még nem kezdődött el, és még nincs helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="cbdf8-153">Védett.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-153">Protected.</span></span>
<span data-ttu-id="cbdf8-154">A védelem folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-154">Protection is ongoing.</span></span>
- <span data-ttu-id="cbdf8-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-155">ProtectionError.</span></span>
<span data-ttu-id="cbdf8-156">Van egy védelmi hiba.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-156">There is a protection error.</span></span>
- <span data-ttu-id="cbdf8-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-157">ProtectionStopped.</span></span>
<span data-ttu-id="cbdf8-158">A védelem le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="cbdf8-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="cbdf8-159">-ProtectionStatus</span></span>

<span data-ttu-id="cbdf8-160">A tároló elemeinek általános védelmi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="cbdf8-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbdf8-162">Egészséges</span><span class="sxs-lookup"><span data-stu-id="cbdf8-162">Healthy</span></span>
- <span data-ttu-id="cbdf8-163">Egészségtelen</span><span class="sxs-lookup"><span data-stu-id="cbdf8-163">Unhealthy</span></span>

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

### <span data-ttu-id="cbdf8-164">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cbdf8-164">-VaultId</span></span>

<span data-ttu-id="cbdf8-165">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="cbdf8-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cbdf8-166">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="cbdf8-166">-WorkloadType</span></span>

<span data-ttu-id="cbdf8-167">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-167">Specifies the workload type.</span></span>
<span data-ttu-id="cbdf8-168">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbdf8-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbdf8-169">AzureVM</span></span>
- <span data-ttu-id="cbdf8-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="cbdf8-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="cbdf8-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="cbdf8-171">AzureFiles</span></span>
- <span data-ttu-id="cbdf8-172">MSSQL</span><span class="sxs-lookup"><span data-stu-id="cbdf8-172">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdf8-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdf8-173">CommonParameters</span></span>
<span data-ttu-id="cbdf8-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbdf8-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdf8-175">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdf8-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdf8-176">INPUTS</span></span>

### <span data-ttu-id="cbdf8-177">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="cbdf8-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="cbdf8-178">System. String</span><span class="sxs-lookup"><span data-stu-id="cbdf8-178">System.String</span></span>

## <span data-ttu-id="cbdf8-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdf8-179">OUTPUTS</span></span>

### <span data-ttu-id="cbdf8-180">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="cbdf8-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="cbdf8-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbdf8-181">NOTES</span></span>

## <span data-ttu-id="cbdf8-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbdf8-182">RELATED LINKS</span></span>

[<span data-ttu-id="cbdf8-183">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cbdf8-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="cbdf8-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="cbdf8-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="cbdf8-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cbdf8-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="cbdf8-186">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cbdf8-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
