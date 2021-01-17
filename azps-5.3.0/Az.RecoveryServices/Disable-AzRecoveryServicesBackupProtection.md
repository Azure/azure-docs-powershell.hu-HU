---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 9dc42a137d3abcd23a64e096117be8d287571ecf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467267"
---
# <span data-ttu-id="3add3-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3add3-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="3add3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3add3-102">SYNOPSIS</span></span>
<span data-ttu-id="3add3-103">Letiltja a biztonsági mentéssel védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="3add3-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="3add3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3add3-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3add3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3add3-105">DESCRIPTION</span></span>
<span data-ttu-id="3add3-106">A **Disable-AzRecoveryServicesBackupProtection** parancsmag letiltja egy Azure biztonsági másolattal védett elem védelmét.</span><span class="sxs-lookup"><span data-stu-id="3add3-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="3add3-107">Ez a parancsmag leállítja egy elem szokásos ütemezett biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="3add3-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="3add3-108">Ez a parancsmag a biztonságimásolat-elem meglévő helyreállítási pontjait is törölheti, ha a RemoveRecoveryPoints paraméterrel végrehajtották.</span><span class="sxs-lookup"><span data-stu-id="3add3-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="3add3-109">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3add3-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3add3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3add3-110">EXAMPLES</span></span>

### <span data-ttu-id="3add3-111">1. példa: A biztonsági mentés védelmének letiltása</span><span class="sxs-lookup"><span data-stu-id="3add3-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="3add3-112">Az első parancs egy tömb biztonságimásolat-tárolót kap, majd a $Cont tárolja.</span><span class="sxs-lookup"><span data-stu-id="3add3-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="3add3-113">A második parancs lekérte az első tárolóelemnek megfelelő biztonságimásolat-elemet, majd tárolja azt a $PI változóban.</span><span class="sxs-lookup"><span data-stu-id="3add3-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="3add3-114">Az utolsó parancs letiltja az elem biztonsági mentésének védelmét a $PI \[ 0-ban, de megőrzi \] az adatokat.</span><span class="sxs-lookup"><span data-stu-id="3add3-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="3add3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="3add3-115">Example 2</span></span>

<span data-ttu-id="3add3-116">Letiltja a biztonsági mentéssel védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="3add3-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="3add3-117">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="3add3-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="3add3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3add3-118">PARAMETERS</span></span>

### <span data-ttu-id="3add3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3add3-119">-DefaultProfile</span></span>
<span data-ttu-id="3add3-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3add3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3add3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3add3-121">-Force</span></span>
<span data-ttu-id="3add3-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3add3-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3add3-123">-Item</span><span class="sxs-lookup"><span data-stu-id="3add3-123">-Item</span></span>
<span data-ttu-id="3add3-124">Megadja azt a biztonságimásolat-elemet, amelynek a parancsmagja letiltja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="3add3-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="3add3-125">**AzureRmRecoveryServicesBackupItem** beszerzéséhez használja a Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3add3-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3add3-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="3add3-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="3add3-127">Azt jelzi, hogy ez a parancsmag törli a meglévő helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="3add3-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3add3-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3add3-128">-VaultId</span></span>
<span data-ttu-id="3add3-129">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3add3-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3add3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3add3-130">-Confirm</span></span>
<span data-ttu-id="3add3-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3add3-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3add3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3add3-132">-WhatIf</span></span>
<span data-ttu-id="3add3-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3add3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3add3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3add3-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3add3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3add3-135">CommonParameters</span></span>
<span data-ttu-id="3add3-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3add3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3add3-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3add3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3add3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3add3-138">INPUTS</span></span>

### <span data-ttu-id="3add3-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="3add3-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="3add3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3add3-140">System.String</span></span>

## <span data-ttu-id="3add3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3add3-141">OUTPUTS</span></span>

### <span data-ttu-id="3add3-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="3add3-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3add3-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3add3-143">NOTES</span></span>

## <span data-ttu-id="3add3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3add3-144">RELATED LINKS</span></span>

[<span data-ttu-id="3add3-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3add3-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="3add3-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3add3-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="3add3-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3add3-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


