---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: b900e9b137c8268969ef1eb715f0b79356abc720
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669625"
---
# <span data-ttu-id="601db-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="601db-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="601db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="601db-102">SYNOPSIS</span></span>
<span data-ttu-id="601db-103">Biztonsági mentési házirend törlése egy boltozatról.</span><span class="sxs-lookup"><span data-stu-id="601db-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="601db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="601db-104">SYNTAX</span></span>

### <span data-ttu-id="601db-105">Házirendnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="601db-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601db-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="601db-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="601db-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="601db-107">DESCRIPTION</span></span>
<span data-ttu-id="601db-108">A **Remove-AzRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági házirendeket töröl a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="601db-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="601db-109">A biztonsági mentési házirendek törlése előtt a házirendnek nem lehet megfelelő biztonsági mentési elemekkel rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="601db-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="601db-110">Mielőtt törli a házirendet, győződjön meg arról, hogy minden társított elemhez társítva van egy másik házirend.</span><span class="sxs-lookup"><span data-stu-id="601db-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="601db-111">Ha egy biztonsági elemmel szeretne másik házirendet társítani, használja az Enable-AzRecoveryServicesBackupProtection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="601db-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="601db-112">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="601db-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="601db-113">Példák</span><span class="sxs-lookup"><span data-stu-id="601db-113">EXAMPLES</span></span>

### <span data-ttu-id="601db-114">1. példa: házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="601db-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="601db-115">Az első parancs megkapja a NewPolicy nevű biztonsági házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="601db-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="601db-116">A második parancs eltávolítja a házirend-objektumot a $Polban.</span><span class="sxs-lookup"><span data-stu-id="601db-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="601db-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="601db-117">PARAMETERS</span></span>

### <span data-ttu-id="601db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601db-118">-DefaultProfile</span></span>
<span data-ttu-id="601db-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="601db-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="601db-120">-Force</span><span class="sxs-lookup"><span data-stu-id="601db-120">-Force</span></span>
<span data-ttu-id="601db-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="601db-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="601db-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="601db-122">-Name</span></span>
<span data-ttu-id="601db-123">Annak a biztonsági mentési házirendnek a neve, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="601db-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="601db-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="601db-124">-PassThru</span></span>
<span data-ttu-id="601db-125">Adja vissza a házirendet, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="601db-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="601db-126">-Házirend</span><span class="sxs-lookup"><span data-stu-id="601db-126">-Policy</span></span>
<span data-ttu-id="601db-127">Az eltávolítandó biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="601db-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="601db-128">**BackupPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="601db-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="601db-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="601db-129">-VaultId</span></span>
<span data-ttu-id="601db-130">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="601db-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="601db-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="601db-131">-Confirm</span></span>
<span data-ttu-id="601db-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="601db-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="601db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="601db-133">-WhatIf</span></span>
<span data-ttu-id="601db-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="601db-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="601db-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="601db-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="601db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601db-136">CommonParameters</span></span>
<span data-ttu-id="601db-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="601db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601db-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="601db-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601db-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="601db-139">INPUTS</span></span>

### <span data-ttu-id="601db-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="601db-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="601db-141">System. String</span><span class="sxs-lookup"><span data-stu-id="601db-141">System.String</span></span>

## <span data-ttu-id="601db-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="601db-142">OUTPUTS</span></span>

### <span data-ttu-id="601db-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="601db-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="601db-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="601db-144">NOTES</span></span>

## <span data-ttu-id="601db-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="601db-145">RELATED LINKS</span></span>

[<span data-ttu-id="601db-146">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="601db-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="601db-147">Új – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="601db-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="601db-148">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="601db-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


