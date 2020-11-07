---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669683"
---
# <span data-ttu-id="1bb44-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="1bb44-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="1bb44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bb44-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb44-103">Ez a parancs a mentett elem (például SQL DB) helyreállítási konfigurációját építi fel.</span><span class="sxs-lookup"><span data-stu-id="1bb44-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="1bb44-104">A konfigurációs objektum minden adatot (például helyreállítási módot) tárol, például a visszaállítás és az alkalmazás konkrét paramétereit, például az SQL cél fizikai elérési útját.</span><span class="sxs-lookup"><span data-stu-id="1bb44-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="1bb44-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bb44-105">SYNTAX</span></span>

### <span data-ttu-id="1bb44-106">RpParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1bb44-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb44-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bb44-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb44-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bb44-108">DESCRIPTION</span></span>
<span data-ttu-id="1bb44-109">A parancs visszaadja az AzureWorkload-elemek helyreállítási konfigurációját, amelyet a visszaállítási parancsmagnak továbbítanak.</span><span class="sxs-lookup"><span data-stu-id="1bb44-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="1bb44-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1bb44-110">EXAMPLES</span></span>

### <span data-ttu-id="1bb44-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1bb44-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="1bb44-112">Az első parancsmag a helyreállítási pont objektum beszerzéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="1bb44-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="1bb44-113">A második parancsmag létrehoz egy helyreállítási tervet az eredeti helyre való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="1bb44-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="1bb44-114">A harmadik parancsmag helyreállítási tervet crreats a másodlagos helyre való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="1bb44-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="1bb44-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bb44-115">PARAMETERS</span></span>

### <span data-ttu-id="1bb44-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="1bb44-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="1bb44-117">Itt adhatja meg, hogy a biztonsági másolatot kapott DB felülírja-e a helyreállítási pontban lévő DB-adatokkal.</span><span class="sxs-lookup"><span data-stu-id="1bb44-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="1bb44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb44-118">-DefaultProfile</span></span>
<span data-ttu-id="1bb44-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bb44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb44-120">-Elem</span><span class="sxs-lookup"><span data-stu-id="1bb44-120">-Item</span></span>
<span data-ttu-id="1bb44-121">Annak a biztonsági mentési elemnek a meghatározása, amelyen a visszaállítási műveletet végrehajtják.</span><span class="sxs-lookup"><span data-stu-id="1bb44-121">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="1bb44-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="1bb44-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="1bb44-123">Itt adhatja meg, hogy a biztonsági másolatot kapott DB felülírja-e a helyreállítási pontban lévő DB-adatokkal.</span><span class="sxs-lookup"><span data-stu-id="1bb44-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="1bb44-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="1bb44-124">-PointInTime</span></span>
<span data-ttu-id="1bb44-125">Annak a időtartománynak a záró időpontja, amelyre a helyreállítási pontot be kell olvasni</span><span class="sxs-lookup"><span data-stu-id="1bb44-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="1bb44-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1bb44-126">-RecoveryPoint</span></span>
<span data-ttu-id="1bb44-127">Visszaállítandó helyreállítási pont objektum</span><span class="sxs-lookup"><span data-stu-id="1bb44-127">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="1bb44-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="1bb44-128">-TargetItem</span></span>
<span data-ttu-id="1bb44-129">Annak a célnak a meghatározása, amelyen a DB-t vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="1bb44-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="1bb44-130">Az SQL visszaállításakor csak a védett elem típusú SQLInstance kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="1bb44-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="1bb44-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1bb44-131">-VaultId</span></span>
<span data-ttu-id="1bb44-132">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="1bb44-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1bb44-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1bb44-133">-Confirm</span></span>
<span data-ttu-id="1bb44-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1bb44-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb44-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb44-135">-WhatIf</span></span>
<span data-ttu-id="1bb44-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1bb44-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb44-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bb44-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb44-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb44-138">CommonParameters</span></span>
<span data-ttu-id="1bb44-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bb44-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb44-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb44-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb44-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb44-141">INPUTS</span></span>

### <span data-ttu-id="1bb44-142">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="1bb44-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="1bb44-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb44-143">System.String</span></span>

## <span data-ttu-id="1bb44-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb44-144">OUTPUTS</span></span>

### <span data-ttu-id="1bb44-145">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="1bb44-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="1bb44-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bb44-146">NOTES</span></span>

## <span data-ttu-id="1bb44-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bb44-147">RELATED LINKS</span></span>