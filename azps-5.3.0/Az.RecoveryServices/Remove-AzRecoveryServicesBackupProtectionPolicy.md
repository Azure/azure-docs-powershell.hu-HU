---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467246"
---
# <span data-ttu-id="13b33-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13b33-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="13b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b33-102">SYNOPSIS</span></span>
<span data-ttu-id="13b33-103">Biztonságimásolat-védelmi házirend törlése egy tárolóból.</span><span class="sxs-lookup"><span data-stu-id="13b33-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="13b33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13b33-104">SYNTAX</span></span>

### <span data-ttu-id="13b33-105">PolicyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13b33-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b33-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="13b33-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b33-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13b33-107">DESCRIPTION</span></span>
<span data-ttu-id="13b33-108">A **Remove-AzRecoveryServicesBackupProtectionPolicy** parancsmag törli a tároló biztonsági mentési házirendeit.</span><span class="sxs-lookup"><span data-stu-id="13b33-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="13b33-109">A biztonságimásolat-védelmi házirendek törlése előtt a házirendhez nem lehet társítva biztonságimásolat-elem.</span><span class="sxs-lookup"><span data-stu-id="13b33-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="13b33-110">A házirend törlése előtt győződjön meg arról, hogy az egyes társított elemek más házirendhez vannak társítva.</span><span class="sxs-lookup"><span data-stu-id="13b33-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="13b33-111">Ha egy biztonságimásolat-elemhez másik házirendet Enable-AzRecoveryServicesBackupProtection társítani.</span><span class="sxs-lookup"><span data-stu-id="13b33-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="13b33-112">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="13b33-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="13b33-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13b33-113">EXAMPLES</span></span>

### <span data-ttu-id="13b33-114">1. példa: Házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="13b33-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="13b33-115">Az első parancs lekérte a NewPolicy nevű biztonságimásolat-védelmi házirendet, majd tárolja azt a $Pol változóban.</span><span class="sxs-lookup"><span data-stu-id="13b33-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="13b33-116">A második parancs eltávolítja a házirendobjektumot a $Pol.</span><span class="sxs-lookup"><span data-stu-id="13b33-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="13b33-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="13b33-117">Example 2</span></span>

<span data-ttu-id="13b33-118">Biztonságimásolat-védelmi házirend törlése egy tárolóból.</span><span class="sxs-lookup"><span data-stu-id="13b33-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="13b33-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="13b33-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="13b33-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b33-120">PARAMETERS</span></span>

### <span data-ttu-id="13b33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b33-121">-DefaultProfile</span></span>
<span data-ttu-id="13b33-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13b33-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13b33-123">-Force</span><span class="sxs-lookup"><span data-stu-id="13b33-123">-Force</span></span>
<span data-ttu-id="13b33-124">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="13b33-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13b33-125">-Name</span><span class="sxs-lookup"><span data-stu-id="13b33-125">-Name</span></span>
<span data-ttu-id="13b33-126">Az eltávolítható biztonságimásolat-védelmi házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13b33-126">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b33-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13b33-127">-PassThru</span></span>
<span data-ttu-id="13b33-128">Adja vissza a törölni akaró házirendet.</span><span class="sxs-lookup"><span data-stu-id="13b33-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="13b33-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="13b33-129">-Policy</span></span>
<span data-ttu-id="13b33-130">Az eltávolítható biztonságimásolat-védelmi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="13b33-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="13b33-131">**BackupPolicy-objektum beszerzéséhez** használja a Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="13b33-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b33-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="13b33-132">-VaultId</span></span>
<span data-ttu-id="13b33-133">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13b33-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="13b33-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13b33-134">-Confirm</span></span>
<span data-ttu-id="13b33-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13b33-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b33-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b33-136">-WhatIf</span></span>
<span data-ttu-id="13b33-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13b33-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="13b33-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b33-138">CommonParameters</span></span>
<span data-ttu-id="13b33-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b33-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b33-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13b33-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b33-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13b33-141">INPUTS</span></span>

### <span data-ttu-id="13b33-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="13b33-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="13b33-143">System.String</span><span class="sxs-lookup"><span data-stu-id="13b33-143">System.String</span></span>

## <span data-ttu-id="13b33-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b33-144">OUTPUTS</span></span>

### <span data-ttu-id="13b33-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="13b33-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="13b33-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13b33-146">NOTES</span></span>

## <span data-ttu-id="13b33-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13b33-147">RELATED LINKS</span></span>

[<span data-ttu-id="13b33-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13b33-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="13b33-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13b33-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="13b33-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13b33-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


