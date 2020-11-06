---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493077"
---
# <span data-ttu-id="0b8aa-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b8aa-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="0b8aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8aa-103">Beolvassa az elemeket egy tárolóból a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b8aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b8aa-104">SYNTAX</span></span>

### <span data-ttu-id="0b8aa-105">GetItemsForContainer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b8aa-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b8aa-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="0b8aa-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b8aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b8aa-107">DESCRIPTION</span></span>
<span data-ttu-id="0b8aa-108">A **Get-AzureRmRecoveryServicesBackupItem** parancsmag a tárolóban lévő elemeket, illetve az Azure biztonsági másolatban szereplő elemeket, valamint az elemek védelmi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="0b8aa-109">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="0b8aa-110">Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy biztonságimásolat-elem lehet.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="0b8aa-111">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0b8aa-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0b8aa-112">EXAMPLES</span></span>

### <span data-ttu-id="0b8aa-113">Példa 1: elem beszerzése biztonsági tárolóból</span><span class="sxs-lookup"><span data-stu-id="0b8aa-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="0b8aa-114">Az első parancs beolvassa a AzureVM típusú dobozt, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="0b8aa-115">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Container, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="0b8aa-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b8aa-116">PARAMETERS</span></span>

### <span data-ttu-id="0b8aa-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0b8aa-117">-BackupManagementType</span></span>
<span data-ttu-id="0b8aa-118">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="0b8aa-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b8aa-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8aa-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0b8aa-120">AzureVM</span></span> 
- <span data-ttu-id="0b8aa-121">MARS</span><span class="sxs-lookup"><span data-stu-id="0b8aa-121">MARS</span></span> 
- <span data-ttu-id="0b8aa-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="0b8aa-122">SCDPM</span></span> 
- <span data-ttu-id="0b8aa-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="0b8aa-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8aa-124">-Container</span><span class="sxs-lookup"><span data-stu-id="0b8aa-124">-Container</span></span>
<span data-ttu-id="0b8aa-125">Azt a tároló objektumot adja meg, amelyből a parancsmag biztonsági mentési elemeket kap.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="0b8aa-126">Ha **AzureRmRecoveryServicesBackupContainer** szeretne beolvasni, használja az Get-AzureRmRecoveryServicesBackupContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8aa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8aa-127">-DefaultProfile</span></span>
<span data-ttu-id="0b8aa-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b8aa-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0b8aa-129">-Name</span></span>
<span data-ttu-id="0b8aa-130">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-130">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8aa-131">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="0b8aa-131">-ProtectionState</span></span>
<span data-ttu-id="0b8aa-132">A védelmi államot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-132">Specifies the state of protection.</span></span>
<span data-ttu-id="0b8aa-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b8aa-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8aa-134">IRPending.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-134">IRPending.</span></span>
<span data-ttu-id="0b8aa-135">A kezdeti szinkronizálás még nem kezdődött el, és még nincs helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-135">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="0b8aa-136">Védett.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-136">Protected.</span></span>
<span data-ttu-id="0b8aa-137">A védelem folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-137">Protection is ongoing.</span></span> 
- <span data-ttu-id="0b8aa-138">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-138">ProtectionError.</span></span>
<span data-ttu-id="0b8aa-139">Van egy védelmi hiba.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-139">There is a protection error.</span></span>
- <span data-ttu-id="0b8aa-140">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-140">ProtectionStopped.</span></span>
<span data-ttu-id="0b8aa-141">A védelem le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-141">Protection is disabled.</span></span>

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8aa-142">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="0b8aa-142">-ProtectionStatus</span></span>
<span data-ttu-id="0b8aa-143">A tároló elemeinek általános védelmi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-143">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="0b8aa-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b8aa-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8aa-145">Egészséges</span><span class="sxs-lookup"><span data-stu-id="0b8aa-145">Healthy</span></span>
- <span data-ttu-id="0b8aa-146">Egészségtelen</span><span class="sxs-lookup"><span data-stu-id="0b8aa-146">Unhealthy</span></span>

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8aa-147">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0b8aa-147">-WorkloadType</span></span>
<span data-ttu-id="0b8aa-148">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-148">Specifies the workload type.</span></span> <span data-ttu-id="0b8aa-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b8aa-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8aa-150">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0b8aa-150">AzureVM</span></span> 
- <span data-ttu-id="0b8aa-151">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="0b8aa-151">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8aa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8aa-152">CommonParameters</span></span>
<span data-ttu-id="0b8aa-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b8aa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8aa-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b8aa-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8aa-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b8aa-155">INPUTS</span></span>

### <span data-ttu-id="0b8aa-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b8aa-156">None</span></span>
<span data-ttu-id="0b8aa-157">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b8aa-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b8aa-158">OUTPUTS</span></span>

### <span data-ttu-id="0b8aa-159">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="0b8aa-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="0b8aa-160">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="0b8aa-160">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="0b8aa-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b8aa-161">NOTES</span></span>

## <span data-ttu-id="0b8aa-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b8aa-162">RELATED LINKS</span></span>

[<span data-ttu-id="0b8aa-163">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b8aa-163">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="0b8aa-164">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0b8aa-164">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="0b8aa-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0b8aa-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="0b8aa-166">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b8aa-166">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


