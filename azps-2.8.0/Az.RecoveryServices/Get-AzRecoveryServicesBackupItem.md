---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838596"
---
# <span data-ttu-id="144b2-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="144b2-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="144b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="144b2-102">SYNOPSIS</span></span>

<span data-ttu-id="144b2-103">Beolvassa az elemeket egy tárolóból a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="144b2-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="144b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="144b2-104">SYNTAX</span></span>

### <span data-ttu-id="144b2-105">GetItemsForContainer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="144b2-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="144b2-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="144b2-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="144b2-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="144b2-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="144b2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="144b2-108">DESCRIPTION</span></span>

<span data-ttu-id="144b2-109">A **Get-AzRecoveryServicesBackupItem** parancsmag a tárolóban lévő elemeket, illetve az Azure biztonsági másolatban szereplő elemeket, valamint az elemek védelmi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="144b2-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="144b2-110">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="144b2-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="144b2-111">Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy biztonságimásolat-elem lehet.</span><span class="sxs-lookup"><span data-stu-id="144b2-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="144b2-112">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="144b2-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="144b2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="144b2-113">EXAMPLES</span></span>

### <span data-ttu-id="144b2-114">Példa 1: elem beszerzése biztonsági tárolóból</span><span class="sxs-lookup"><span data-stu-id="144b2-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="144b2-115">Az első parancs beolvassa a AzureVM típusú dobozt, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="144b2-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="144b2-116">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Container, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="144b2-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="144b2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="144b2-117">PARAMETERS</span></span>

### <span data-ttu-id="144b2-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="144b2-118">-BackupManagementType</span></span>

<span data-ttu-id="144b2-119">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="144b2-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="144b2-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="144b2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="144b2-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="144b2-121">AzureVM</span></span>
- <span data-ttu-id="144b2-122">MARS</span><span class="sxs-lookup"><span data-stu-id="144b2-122">MARS</span></span>
- <span data-ttu-id="144b2-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="144b2-123">SCDPM</span></span>
- <span data-ttu-id="144b2-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="144b2-124">AzureBackupServer</span></span>
- <span data-ttu-id="144b2-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="144b2-125">AzureSQL</span></span>
- <span data-ttu-id="144b2-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="144b2-126">AzureStorage</span></span>
- <span data-ttu-id="144b2-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="144b2-127">AzureWorkload</span></span>

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

### <span data-ttu-id="144b2-128">-Container</span><span class="sxs-lookup"><span data-stu-id="144b2-128">-Container</span></span>

<span data-ttu-id="144b2-129">Azt a tároló objektumot adja meg, amelyből a parancsmag biztonsági mentési elemeket kap.</span><span class="sxs-lookup"><span data-stu-id="144b2-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="144b2-130">**AzureRmRecoveryServicesBackupContainer** beszerzéséhez használja a **Get-AzRecoveryServicesBackupContainer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="144b2-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="144b2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144b2-131">-DefaultProfile</span></span>

<span data-ttu-id="144b2-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="144b2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="144b2-133">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="144b2-133">-DeleteState</span></span>
<span data-ttu-id="144b2-134">Az elem deletestate adja meg, hogy a paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="144b2-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="144b2-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="144b2-135">ToBeDeleted</span></span>
- <span data-ttu-id="144b2-136">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="144b2-136">NotDeleted</span></span>

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

### <span data-ttu-id="144b2-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="144b2-137">-Name</span></span>

<span data-ttu-id="144b2-138">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="144b2-138">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="144b2-139">-Házirend</span><span class="sxs-lookup"><span data-stu-id="144b2-139">-Policy</span></span>

<span data-ttu-id="144b2-140">Protection Policy objektum.</span><span class="sxs-lookup"><span data-stu-id="144b2-140">Protection policy object.</span></span>

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

### <span data-ttu-id="144b2-141">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="144b2-141">-ProtectionState</span></span>

<span data-ttu-id="144b2-142">A védelmi államot adja meg.</span><span class="sxs-lookup"><span data-stu-id="144b2-142">Specifies the state of protection.</span></span>
<span data-ttu-id="144b2-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="144b2-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="144b2-144">IRPending.</span><span class="sxs-lookup"><span data-stu-id="144b2-144">IRPending.</span></span>
<span data-ttu-id="144b2-145">A kezdeti szinkronizálás még nem kezdődött el, és még nincs helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="144b2-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="144b2-146">Védett.</span><span class="sxs-lookup"><span data-stu-id="144b2-146">Protected.</span></span>
<span data-ttu-id="144b2-147">A védelem folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="144b2-147">Protection is ongoing.</span></span>
- <span data-ttu-id="144b2-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="144b2-148">ProtectionError.</span></span>
<span data-ttu-id="144b2-149">Van egy védelmi hiba.</span><span class="sxs-lookup"><span data-stu-id="144b2-149">There is a protection error.</span></span>
- <span data-ttu-id="144b2-150">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="144b2-150">ProtectionStopped.</span></span>
<span data-ttu-id="144b2-151">A védelem le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="144b2-151">Protection is disabled.</span></span>

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

### <span data-ttu-id="144b2-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="144b2-152">-ProtectionStatus</span></span>

<span data-ttu-id="144b2-153">A tároló elemeinek általános védelmi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="144b2-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="144b2-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="144b2-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="144b2-155">Egészséges</span><span class="sxs-lookup"><span data-stu-id="144b2-155">Healthy</span></span>
- <span data-ttu-id="144b2-156">Egészségtelen</span><span class="sxs-lookup"><span data-stu-id="144b2-156">Unhealthy</span></span>

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

### <span data-ttu-id="144b2-157">-VaultId</span><span class="sxs-lookup"><span data-stu-id="144b2-157">-VaultId</span></span>

<span data-ttu-id="144b2-158">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="144b2-158">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="144b2-159">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="144b2-159">-WorkloadType</span></span>

<span data-ttu-id="144b2-160">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="144b2-160">Specifies the workload type.</span></span>
<span data-ttu-id="144b2-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="144b2-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="144b2-162">AzureVM</span><span class="sxs-lookup"><span data-stu-id="144b2-162">AzureVM</span></span>
- <span data-ttu-id="144b2-163">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="144b2-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="144b2-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="144b2-164">AzureFiles</span></span>
- <span data-ttu-id="144b2-165">MSSQL</span><span class="sxs-lookup"><span data-stu-id="144b2-165">MSSQL</span></span>

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

### <span data-ttu-id="144b2-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144b2-166">-CommonParameters</span></span>

<span data-ttu-id="144b2-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="144b2-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144b2-168">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="144b2-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144b2-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="144b2-169">INPUTS</span></span>

### <span data-ttu-id="144b2-170">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="144b2-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="144b2-171">System. String</span><span class="sxs-lookup"><span data-stu-id="144b2-171">System.String</span></span>

## <span data-ttu-id="144b2-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="144b2-172">OUTPUTS</span></span>

### <span data-ttu-id="144b2-173">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="144b2-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="144b2-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="144b2-174">NOTES</span></span>

## <span data-ttu-id="144b2-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="144b2-175">RELATED LINKS</span></span>

[<span data-ttu-id="144b2-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="144b2-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="144b2-177">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="144b2-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="144b2-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="144b2-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="144b2-179">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="144b2-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
