---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: bb0f3b18697b3f9e17b8e1744361346e68c47357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922738"
---
# <span data-ttu-id="8e5fa-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8e5fa-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="8e5fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5fa-103">Letiltja a biztonsági mentéssel védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="8e5fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e5fa-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e5fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="8e5fa-106">A **Disable-AzRecoveryServicesBackupProtection** parancsmag letiltja az Azure biztonsági mentéssel védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="8e5fa-107">Ez a parancsmag leállítja egy elem szokásos ütemezett biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="8e5fa-108">Ez a parancsmag a biztonságimásolat-elem meglévő helyreállítási pontjait is törölheti, ha a RemoveRecoveryPoints paraméterrel végrehajtja őket.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="8e5fa-109">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8e5fa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e5fa-110">EXAMPLES</span></span>

### <span data-ttu-id="8e5fa-111">1. példa: A biztonsági mentés védelmének letiltása</span><span class="sxs-lookup"><span data-stu-id="8e5fa-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="8e5fa-112">Az első parancs egy tömb biztonságimásolat-tárolót kap, majd a $Cont tárolja.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="8e5fa-113">A második parancs lekérte az első tárolóelemnek megfelelő biztonságimásolat-elemet, majd tárolja azt a $PI változóban.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="8e5fa-114">Az utolsó parancs letiltja az elem biztonsági mentésének védelmét a $PI \[ 0-ban, de megőrzi \] az adatokat.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="8e5fa-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="8e5fa-115">Example 2</span></span>

<span data-ttu-id="8e5fa-116">Letiltja a biztonsági mentéssel védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="8e5fa-117">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="8e5fa-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="8e5fa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e5fa-118">PARAMETERS</span></span>

### <span data-ttu-id="8e5fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5fa-119">-DefaultProfile</span></span>
<span data-ttu-id="8e5fa-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e5fa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8e5fa-121">-Force</span></span>
<span data-ttu-id="8e5fa-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e5fa-123">-Item</span><span class="sxs-lookup"><span data-stu-id="8e5fa-123">-Item</span></span>
<span data-ttu-id="8e5fa-124">Megadja azt a biztonságimásolat-elemet, amelynek a parancsmagja letiltja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="8e5fa-125">**AzureRmRecoveryServicesBackupItem** beszerzéséhez használja a Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="8e5fa-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="8e5fa-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="8e5fa-127">Azt jelzi, hogy ez a parancsmag törli a meglévő helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

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

### <span data-ttu-id="8e5fa-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8e5fa-128">-VaultId</span></span>
<span data-ttu-id="8e5fa-129">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8e5fa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e5fa-130">-Confirm</span></span>
<span data-ttu-id="8e5fa-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e5fa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e5fa-132">-WhatIf</span></span>
<span data-ttu-id="8e5fa-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e5fa-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e5fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5fa-135">CommonParameters</span></span>
<span data-ttu-id="8e5fa-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5fa-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e5fa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5fa-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e5fa-138">INPUTS</span></span>

### <span data-ttu-id="8e5fa-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="8e5fa-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="8e5fa-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8e5fa-140">System.String</span></span>

## <span data-ttu-id="8e5fa-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e5fa-141">OUTPUTS</span></span>

### <span data-ttu-id="8e5fa-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="8e5fa-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8e5fa-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e5fa-143">NOTES</span></span>

## <span data-ttu-id="8e5fa-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e5fa-144">RELATED LINKS</span></span>

[<span data-ttu-id="8e5fa-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8e5fa-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="8e5fa-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8e5fa-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="8e5fa-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8e5fa-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


