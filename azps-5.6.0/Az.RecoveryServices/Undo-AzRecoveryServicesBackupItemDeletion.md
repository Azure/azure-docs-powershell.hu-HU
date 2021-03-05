---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: f7e82c2ccc939b0492575766c621a81ef9a25e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011765"
---
# <span data-ttu-id="fdaf6-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="fdaf6-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="fdaf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="fdaf6-103">Ha egy biztonságimásolat-elemet törölnek, és soft-deleted állapotban vannak, ez a parancs visszahozza az elemet egy olyan állapotba, ahol az adatok örökre megmaradnak</span><span class="sxs-lookup"><span data-stu-id="fdaf6-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="fdaf6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fdaf6-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdaf6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fdaf6-105">DESCRIPTION</span></span>
<span data-ttu-id="fdaf6-106">A Undo-AzRecoveryServicesBackupItemDeletion parancsmag visszaállítja a visszaállíthatóan törölt elemet egy olyan állapotba, ahol a védelem leállt, de az adatok örökre megmaradnak.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="fdaf6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fdaf6-107">EXAMPLES</span></span>

### <span data-ttu-id="fdaf6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fdaf6-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="fdaf6-109">Az első parancs egy tömb biztonságimásolat-tárolót kap, majd a $Cont tárolja.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="fdaf6-110">A második parancs lekérte az első tárolóelemnek megfelelő biztonságimásolat-elemet, majd tárolja azt a $PI változóban.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="fdaf6-111">A harmadik parancs letiltja a biztonsági mentés elleni védelmet az $PI 0-ban, és az elemet \[ \] lágyan törölt állapotba helyezi.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="fdaf6-112">A negyedik parancs lekérte az elemet, amely softdeleted állapotban van.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="fdaf6-113">Az utolsó parancs a softdeleted VM-et olyan állapotba hozza, ahol a védelmet leállították, de az adatokat örökre megőrizzük.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="fdaf6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="fdaf6-114">Example 2</span></span>

<span data-ttu-id="fdaf6-115">Rehidratál egy soft-törölt elemet.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="fdaf6-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="fdaf6-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="fdaf6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdaf6-117">PARAMETERS</span></span>

### <span data-ttu-id="fdaf6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdaf6-118">-DefaultProfile</span></span>
<span data-ttu-id="fdaf6-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdaf6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fdaf6-120">-Force</span></span>
<span data-ttu-id="fdaf6-121">Kényszeríti a biztonsági mentés védelmét (megakadályozza a megerősítést kérő párbeszédpanelt).</span><span class="sxs-lookup"><span data-stu-id="fdaf6-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="fdaf6-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="fdaf6-123">-Item</span><span class="sxs-lookup"><span data-stu-id="fdaf6-123">-Item</span></span>
<span data-ttu-id="fdaf6-124">Megadja azt a biztonságimásolat-elemet, amelynek a parancsmagja visszaállítja a törlést.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="fdaf6-125">AzureRmRecoveryServicesBackupItem beszerzéséhez használja a Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="fdaf6-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fdaf6-126">-VaultId</span></span>
<span data-ttu-id="fdaf6-127">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fdaf6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdaf6-128">-Confirm</span></span>
<span data-ttu-id="fdaf6-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdaf6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdaf6-130">-WhatIf</span></span>
<span data-ttu-id="fdaf6-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdaf6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdaf6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdaf6-133">CommonParameters</span></span>
<span data-ttu-id="fdaf6-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdaf6-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdaf6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdaf6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdaf6-136">INPUTS</span></span>

### <span data-ttu-id="fdaf6-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="fdaf6-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="fdaf6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fdaf6-138">System.String</span></span>

## <span data-ttu-id="fdaf6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdaf6-139">OUTPUTS</span></span>

### <span data-ttu-id="fdaf6-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="fdaf6-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="fdaf6-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fdaf6-141">NOTES</span></span>

## <span data-ttu-id="fdaf6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdaf6-142">RELATED LINKS</span></span>

[<span data-ttu-id="fdaf6-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fdaf6-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="fdaf6-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="fdaf6-144">Get-AzRecoveryServicesBackupItem</span></span>]()

