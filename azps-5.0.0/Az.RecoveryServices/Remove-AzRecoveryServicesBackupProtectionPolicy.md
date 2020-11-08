---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188025"
---
# <span data-ttu-id="fda3c-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda3c-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="fda3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fda3c-102">SYNOPSIS</span></span>
<span data-ttu-id="fda3c-103">Biztonsági mentési házirend törlése egy boltozatról.</span><span class="sxs-lookup"><span data-stu-id="fda3c-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="fda3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fda3c-104">SYNTAX</span></span>

### <span data-ttu-id="fda3c-105">Házirendnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fda3c-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda3c-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="fda3c-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda3c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fda3c-107">DESCRIPTION</span></span>
<span data-ttu-id="fda3c-108">A **Remove-AzRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági házirendeket töröl a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="fda3c-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="fda3c-109">A biztonsági mentési házirendek törlése előtt a házirendnek nem lehet megfelelő biztonsági mentési elemekkel rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="fda3c-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="fda3c-110">Mielőtt törli a házirendet, győződjön meg arról, hogy minden társított elemhez társítva van egy másik házirend.</span><span class="sxs-lookup"><span data-stu-id="fda3c-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="fda3c-111">Ha egy biztonsági elemmel szeretne másik házirendet társítani, használja az Enable-AzRecoveryServicesBackupProtection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fda3c-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="fda3c-112">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="fda3c-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fda3c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="fda3c-113">EXAMPLES</span></span>

### <span data-ttu-id="fda3c-114">1. példa: házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fda3c-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="fda3c-115">Az első parancs megkapja a NewPolicy nevű biztonsági házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fda3c-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="fda3c-116">A második parancs eltávolítja a házirend-objektumot a $Polban.</span><span class="sxs-lookup"><span data-stu-id="fda3c-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="fda3c-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="fda3c-117">Example 2</span></span>

<span data-ttu-id="fda3c-118">Biztonsági mentési házirend törlése egy boltozatról.</span><span class="sxs-lookup"><span data-stu-id="fda3c-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="fda3c-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="fda3c-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="fda3c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fda3c-120">PARAMETERS</span></span>

### <span data-ttu-id="fda3c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda3c-121">-DefaultProfile</span></span>
<span data-ttu-id="fda3c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fda3c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fda3c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fda3c-123">-Force</span></span>
<span data-ttu-id="fda3c-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fda3c-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fda3c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fda3c-125">-Name</span></span>
<span data-ttu-id="fda3c-126">Annak a biztonsági mentési házirendnek a neve, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="fda3c-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="fda3c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fda3c-127">-PassThru</span></span>
<span data-ttu-id="fda3c-128">Adja vissza a házirendet, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="fda3c-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="fda3c-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="fda3c-129">-Policy</span></span>
<span data-ttu-id="fda3c-130">Az eltávolítandó biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="fda3c-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="fda3c-131">**BackupPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fda3c-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="fda3c-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fda3c-132">-VaultId</span></span>
<span data-ttu-id="fda3c-133">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="fda3c-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fda3c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fda3c-134">-Confirm</span></span>
<span data-ttu-id="fda3c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fda3c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda3c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda3c-136">-WhatIf</span></span>
<span data-ttu-id="fda3c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fda3c-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="fda3c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda3c-138">CommonParameters</span></span>
<span data-ttu-id="fda3c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fda3c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda3c-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fda3c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda3c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fda3c-141">INPUTS</span></span>

### <span data-ttu-id="fda3c-142">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="fda3c-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="fda3c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fda3c-143">System.String</span></span>

## <span data-ttu-id="fda3c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fda3c-144">OUTPUTS</span></span>

### <span data-ttu-id="fda3c-145">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="fda3c-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="fda3c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fda3c-146">NOTES</span></span>

## <span data-ttu-id="fda3c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fda3c-147">RELATED LINKS</span></span>

[<span data-ttu-id="fda3c-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda3c-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fda3c-149">Új – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda3c-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fda3c-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda3c-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

