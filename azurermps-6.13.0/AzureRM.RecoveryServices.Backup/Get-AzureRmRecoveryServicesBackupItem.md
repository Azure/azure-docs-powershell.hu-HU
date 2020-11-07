---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a1037f742fab47ae84edae6e1558e313e563c25a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679526"
---
# <span data-ttu-id="59fa6-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="59fa6-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="59fa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="59fa6-103">Beolvassa az elemeket egy tárolóból a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="59fa6-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59fa6-104">SYNTAX</span></span>

### <span data-ttu-id="59fa6-105">GetItemsForContainer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59fa6-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59fa6-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="59fa6-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59fa6-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="59fa6-107">GetItemsForPolicy</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59fa6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="59fa6-108">DESCRIPTION</span></span>
<span data-ttu-id="59fa6-109">A **Get-AzureRmRecoveryServicesBackupItem** parancsmag a tárolóban lévő elemeket, illetve az Azure biztonsági másolatban szereplő elemeket, valamint az elemek védelmi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59fa6-109">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="59fa6-110">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="59fa6-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="59fa6-111">Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy biztonságimásolat-elem lehet.</span><span class="sxs-lookup"><span data-stu-id="59fa6-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="59fa6-112">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="59fa6-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="59fa6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="59fa6-113">EXAMPLES</span></span>

### <span data-ttu-id="59fa6-114">Példa 1: elem beszerzése biztonsági tárolóból</span><span class="sxs-lookup"><span data-stu-id="59fa6-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="59fa6-115">Az első parancs beolvassa a AzureVM típusú dobozt, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="59fa6-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="59fa6-116">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Container, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="59fa6-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="59fa6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59fa6-117">PARAMETERS</span></span>

### <span data-ttu-id="59fa6-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="59fa6-118">-BackupManagementType</span></span>
<span data-ttu-id="59fa6-119">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fa6-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="59fa6-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="59fa6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fa6-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="59fa6-121">AzureVM</span></span> 
- <span data-ttu-id="59fa6-122">MARS</span><span class="sxs-lookup"><span data-stu-id="59fa6-122">MARS</span></span> 
- <span data-ttu-id="59fa6-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="59fa6-123">SCDPM</span></span> 
- <span data-ttu-id="59fa6-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="59fa6-124">AzureBackupServer</span></span> 
- <span data-ttu-id="59fa6-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="59fa6-125">AzureSQL</span></span>
- <span data-ttu-id="59fa6-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="59fa6-126">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fa6-127">-Container</span><span class="sxs-lookup"><span data-stu-id="59fa6-127">-Container</span></span>
<span data-ttu-id="59fa6-128">Azt a tároló objektumot adja meg, amelyből a parancsmag biztonsági mentési elemeket kap.</span><span class="sxs-lookup"><span data-stu-id="59fa6-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="59fa6-129">Ha **AzureRmRecoveryServicesBackupContainer** szeretne beolvasni, használja az Get-AzureRmRecoveryServicesBackupContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="59fa6-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="59fa6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fa6-130">-DefaultProfile</span></span>
<span data-ttu-id="59fa6-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59fa6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fa6-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59fa6-132">-Name</span></span>
<span data-ttu-id="59fa6-133">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fa6-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="59fa6-134">-Házirend</span><span class="sxs-lookup"><span data-stu-id="59fa6-134">-Policy</span></span>
<span data-ttu-id="59fa6-135">Protection Policy objektum.</span><span class="sxs-lookup"><span data-stu-id="59fa6-135">Protection policy object.</span></span>

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

### <span data-ttu-id="59fa6-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="59fa6-136">-ProtectionState</span></span>
<span data-ttu-id="59fa6-137">A védelmi államot adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fa6-137">Specifies the state of protection.</span></span>
<span data-ttu-id="59fa6-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="59fa6-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fa6-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="59fa6-139">IRPending.</span></span>
<span data-ttu-id="59fa6-140">A kezdeti szinkronizálás még nem kezdődött el, és még nincs helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="59fa6-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="59fa6-141">Védett.</span><span class="sxs-lookup"><span data-stu-id="59fa6-141">Protected.</span></span>
<span data-ttu-id="59fa6-142">A védelem folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="59fa6-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="59fa6-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="59fa6-143">ProtectionError.</span></span>
<span data-ttu-id="59fa6-144">Van egy védelmi hiba.</span><span class="sxs-lookup"><span data-stu-id="59fa6-144">There is a protection error.</span></span>
- <span data-ttu-id="59fa6-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="59fa6-145">ProtectionStopped.</span></span>
<span data-ttu-id="59fa6-146">A védelem le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="59fa6-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="59fa6-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="59fa6-147">-ProtectionStatus</span></span>
<span data-ttu-id="59fa6-148">A tároló elemeinek általános védelmi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fa6-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="59fa6-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="59fa6-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fa6-150">Egészséges</span><span class="sxs-lookup"><span data-stu-id="59fa6-150">Healthy</span></span>
- <span data-ttu-id="59fa6-151">Egészségtelen</span><span class="sxs-lookup"><span data-stu-id="59fa6-151">Unhealthy</span></span>

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

### <span data-ttu-id="59fa6-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="59fa6-152">-VaultId</span></span>
<span data-ttu-id="59fa6-153">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="59fa6-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="59fa6-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="59fa6-154">-WorkloadType</span></span>
<span data-ttu-id="59fa6-155">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fa6-155">Specifies the workload type.</span></span> <span data-ttu-id="59fa6-156">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="59fa6-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fa6-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="59fa6-157">AzureVM</span></span> 
- <span data-ttu-id="59fa6-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="59fa6-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="59fa6-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="59fa6-159">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fa6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fa6-160">CommonParameters</span></span>
<span data-ttu-id="59fa6-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59fa6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fa6-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fa6-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fa6-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59fa6-163">INPUTS</span></span>

### <span data-ttu-id="59fa6-164">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="59fa6-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="59fa6-165">System. String</span><span class="sxs-lookup"><span data-stu-id="59fa6-165">System.String</span></span>
<span data-ttu-id="59fa6-166">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59fa6-166">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="59fa6-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59fa6-167">OUTPUTS</span></span>

### <span data-ttu-id="59fa6-168">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="59fa6-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="59fa6-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59fa6-169">NOTES</span></span>

## <span data-ttu-id="59fa6-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59fa6-170">RELATED LINKS</span></span>

[<span data-ttu-id="59fa6-171">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="59fa6-171">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="59fa6-172">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="59fa6-172">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="59fa6-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="59fa6-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="59fa6-174">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="59fa6-174">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


