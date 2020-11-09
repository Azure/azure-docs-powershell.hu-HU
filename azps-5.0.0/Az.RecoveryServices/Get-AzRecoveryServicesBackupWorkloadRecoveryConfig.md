---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303000"
---
# <span data-ttu-id="a89fc-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="a89fc-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="a89fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a89fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a89fc-103">Ez a parancs a mentett elem (például SQL DB) helyreállítási konfigurációját építi fel.</span><span class="sxs-lookup"><span data-stu-id="a89fc-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="a89fc-104">A konfigurációs objektum minden adatot (például helyreállítási módot) tárol, például a visszaállítás és az alkalmazás konkrét paramétereit, például az SQL cél fizikai elérési útját.</span><span class="sxs-lookup"><span data-stu-id="a89fc-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="a89fc-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a89fc-105">SYNTAX</span></span>

### <span data-ttu-id="a89fc-106">RpParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a89fc-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a89fc-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89fc-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a89fc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a89fc-108">DESCRIPTION</span></span>
<span data-ttu-id="a89fc-109">A parancs visszaadja az AzureWorkload-elemek helyreállítási konfigurációját, amelyet a visszaállítási parancsmagnak továbbítanak.</span><span class="sxs-lookup"><span data-stu-id="a89fc-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="a89fc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a89fc-110">EXAMPLES</span></span>

### <span data-ttu-id="a89fc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a89fc-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="a89fc-112">Az első parancsmag a helyreállítási pont objektum beszerzéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="a89fc-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="a89fc-113">A második parancsmag létrehoz egy helyreállítási tervet az eredeti helyre való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="a89fc-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="a89fc-114">A harmadik parancsmag helyreállítási tervet hoz létre a másodlagos helyre való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="a89fc-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="a89fc-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="a89fc-115">Example 2</span></span>

<span data-ttu-id="a89fc-116">Ez a parancs a mentett elem (például SQL DB) helyreállítási konfigurációját építi fel.</span><span class="sxs-lookup"><span data-stu-id="a89fc-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="a89fc-117">autogenerated</span><span class="sxs-lookup"><span data-stu-id="a89fc-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="a89fc-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a89fc-118">PARAMETERS</span></span>

### <span data-ttu-id="a89fc-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="a89fc-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="a89fc-120">Azt adja meg, hogy a biztonsági másolatban lévő biztonsági másolatot vissza kell-e állítani egy másik kijelölt kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="a89fc-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="a89fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89fc-121">-DefaultProfile</span></span>
<span data-ttu-id="a89fc-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a89fc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a89fc-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a89fc-123">-FilePath</span></span>
<span data-ttu-id="a89fc-124">A visszaállítási művelethez használt filepath adja meg.</span><span class="sxs-lookup"><span data-stu-id="a89fc-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="a89fc-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="a89fc-125">-FromFull</span></span>
<span data-ttu-id="a89fc-126">Annak a teljes RecoveryPoint adja meg, amelyre a naplózási biztonsági másolatok érvényesek lesznek.</span><span class="sxs-lookup"><span data-stu-id="a89fc-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89fc-127">-Elem</span><span class="sxs-lookup"><span data-stu-id="a89fc-127">-Item</span></span>
<span data-ttu-id="a89fc-128">Annak a biztonsági mentési elemnek a meghatározása, amelyen a visszaállítási műveletet végrehajtják.</span><span class="sxs-lookup"><span data-stu-id="a89fc-128">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89fc-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="a89fc-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="a89fc-130">Itt adhatja meg, hogy a biztonsági másolatot kapott DB felülírja-e a helyreállítási pontban lévő DB-adatokkal.</span><span class="sxs-lookup"><span data-stu-id="a89fc-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="a89fc-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="a89fc-131">-PointInTime</span></span>
<span data-ttu-id="a89fc-132">Annak a időtartománynak a záró időpontja, amelyre a helyreállítási pontot be kell olvasni</span><span class="sxs-lookup"><span data-stu-id="a89fc-132">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89fc-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a89fc-133">-RecoveryPoint</span></span>
<span data-ttu-id="a89fc-134">Visszaállítandó helyreállítási pont objektum</span><span class="sxs-lookup"><span data-stu-id="a89fc-134">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a89fc-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="a89fc-135">-RestoreAsFiles</span></span>
<span data-ttu-id="a89fc-136">Az adatbázis fájlokként való visszaállítását adja meg a számítógépen.</span><span class="sxs-lookup"><span data-stu-id="a89fc-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="a89fc-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="a89fc-137">-TargetContainer</span></span>
<span data-ttu-id="a89fc-138">Azt a célszámítógép-fájlt adja vissza, amelyen a DB-fájlokat vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="a89fc-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89fc-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="a89fc-139">-TargetItem</span></span>
<span data-ttu-id="a89fc-140">Annak a célnak a meghatározása, amelyen a DB-t vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="a89fc-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="a89fc-141">Az SQL visszaállításakor csak a védett elem típusú SQLInstance kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="a89fc-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89fc-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a89fc-142">-VaultId</span></span>
<span data-ttu-id="a89fc-143">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="a89fc-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a89fc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89fc-144">CommonParameters</span></span>
<span data-ttu-id="a89fc-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a89fc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89fc-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a89fc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89fc-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a89fc-147">INPUTS</span></span>

### <span data-ttu-id="a89fc-148">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a89fc-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="a89fc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a89fc-149">System.String</span></span>

## <span data-ttu-id="a89fc-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a89fc-150">OUTPUTS</span></span>

### <span data-ttu-id="a89fc-151">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="a89fc-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="a89fc-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a89fc-152">NOTES</span></span>

## <span data-ttu-id="a89fc-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a89fc-153">RELATED LINKS</span></span>
