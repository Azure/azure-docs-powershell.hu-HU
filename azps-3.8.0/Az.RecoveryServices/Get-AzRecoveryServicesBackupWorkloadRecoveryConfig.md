---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014720"
---
# <span data-ttu-id="07be1-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="07be1-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="07be1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07be1-102">SYNOPSIS</span></span>
<span data-ttu-id="07be1-103">Ez a parancs a mentett elem (például SQL DB) helyreállítási konfigurációját építi fel.</span><span class="sxs-lookup"><span data-stu-id="07be1-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="07be1-104">A konfigurációs objektum minden adatot (például helyreállítási módot) tárol, például a visszaállítás és az alkalmazás konkrét paramétereit, például az SQL cél fizikai elérési útját.</span><span class="sxs-lookup"><span data-stu-id="07be1-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="07be1-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07be1-105">SYNTAX</span></span>

### <span data-ttu-id="07be1-106">RpParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07be1-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07be1-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="07be1-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07be1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="07be1-108">DESCRIPTION</span></span>
<span data-ttu-id="07be1-109">A parancs visszaadja az AzureWorkload-elemek helyreállítási konfigurációját, amelyet a visszaállítási parancsmagnak továbbítanak.</span><span class="sxs-lookup"><span data-stu-id="07be1-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="07be1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="07be1-110">EXAMPLES</span></span>

### <span data-ttu-id="07be1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07be1-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="07be1-112">Az első parancsmag a helyreállítási pont objektum beszerzéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="07be1-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="07be1-113">A második parancsmag létrehoz egy helyreállítási tervet az eredeti helyre való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="07be1-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="07be1-114">A harmadik parancsmag helyreállítási tervet hoz létre a másodlagos helyre való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="07be1-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="07be1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07be1-115">PARAMETERS</span></span>

### <span data-ttu-id="07be1-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="07be1-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="07be1-117">Itt adhatja meg, hogy a biztonsági másolatot kapott DB felülírja-e a helyreállítási pontban lévő DB-adatokkal.</span><span class="sxs-lookup"><span data-stu-id="07be1-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="07be1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07be1-118">-DefaultProfile</span></span>
<span data-ttu-id="07be1-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07be1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07be1-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="07be1-120">-FilePath</span></span>
<span data-ttu-id="07be1-121">A visszaállítási művelet filepath adja meg.</span><span class="sxs-lookup"><span data-stu-id="07be1-121">Specifies the filepath for restore operation.</span></span>

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

### <span data-ttu-id="07be1-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="07be1-122">-FromFull</span></span>
<span data-ttu-id="07be1-123">Annak a teljes RecoveryPoint adja meg, amelyre a naplózási biztonsági másolatok érvényesek lesznek.</span><span class="sxs-lookup"><span data-stu-id="07be1-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="07be1-124">-Elem</span><span class="sxs-lookup"><span data-stu-id="07be1-124">-Item</span></span>
<span data-ttu-id="07be1-125">Annak a biztonsági mentési elemnek a meghatározása, amelyen a visszaállítási műveletet végrehajtják.</span><span class="sxs-lookup"><span data-stu-id="07be1-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="07be1-126">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="07be1-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="07be1-127">Itt adhatja meg, hogy a biztonsági másolatot kapott DB felülírja-e a helyreállítási pontban lévő DB-adatokkal.</span><span class="sxs-lookup"><span data-stu-id="07be1-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="07be1-128">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="07be1-128">-PointInTime</span></span>
<span data-ttu-id="07be1-129">Annak a időtartománynak a záró időpontja, amelyre a helyreállítási pontot be kell olvasni</span><span class="sxs-lookup"><span data-stu-id="07be1-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="07be1-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="07be1-130">-RecoveryPoint</span></span>
<span data-ttu-id="07be1-131">Visszaállítandó helyreállítási pont objektum</span><span class="sxs-lookup"><span data-stu-id="07be1-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="07be1-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="07be1-132">-RestoreAsFiles</span></span>
<span data-ttu-id="07be1-133">Az adatbázis fájlokként való visszaállítását adja meg a számítógépen.</span><span class="sxs-lookup"><span data-stu-id="07be1-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="07be1-134">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="07be1-134">-TargetContainer</span></span>
<span data-ttu-id="07be1-135">Azt a célszámítógép-fájlt adja vissza, amelyen a DB-fájlokat vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="07be1-135">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="07be1-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="07be1-136">-TargetItem</span></span>
<span data-ttu-id="07be1-137">Annak a célnak a meghatározása, amelyen a DB-t vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="07be1-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="07be1-138">Az SQL visszaállításakor csak a védett elem típusú SQLInstance kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="07be1-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="07be1-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="07be1-139">-VaultId</span></span>
<span data-ttu-id="07be1-140">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="07be1-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="07be1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07be1-141">CommonParameters</span></span>
<span data-ttu-id="07be1-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07be1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07be1-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07be1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07be1-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07be1-144">INPUTS</span></span>

### <span data-ttu-id="07be1-145">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="07be1-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="07be1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="07be1-146">System.String</span></span>

## <span data-ttu-id="07be1-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07be1-147">OUTPUTS</span></span>

### <span data-ttu-id="07be1-148">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="07be1-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="07be1-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07be1-149">NOTES</span></span>

## <span data-ttu-id="07be1-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07be1-150">RELATED LINKS</span></span>
