---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 805deece859eb4baa05d8c3d34dfcc8a9d571354
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504288"
---
# <span data-ttu-id="4af1a-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4af1a-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="4af1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4af1a-102">SYNOPSIS</span></span>
<span data-ttu-id="4af1a-103">Biztonsági mentési házirend törlése egy boltozatról.</span><span class="sxs-lookup"><span data-stu-id="4af1a-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4af1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4af1a-104">SYNTAX</span></span>

### <span data-ttu-id="4af1a-105">Házirendnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4af1a-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4af1a-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="4af1a-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4af1a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4af1a-107">DESCRIPTION</span></span>
<span data-ttu-id="4af1a-108">A **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági házirendeket töröl a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="4af1a-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="4af1a-109">A biztonsági mentési házirendek törlése előtt a házirendnek nem lehet megfelelő biztonsági mentési elemekkel rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="4af1a-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="4af1a-110">Mielőtt törli a házirendet, győződjön meg arról, hogy minden társított elemhez társítva van egy másik házirend.</span><span class="sxs-lookup"><span data-stu-id="4af1a-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="4af1a-111">Ha egy biztonsági elemmel szeretne másik házirendet társítani, használja az Enable-AzureRmRecoveryServicesBackupProtection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4af1a-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="4af1a-112">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="4af1a-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4af1a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4af1a-113">EXAMPLES</span></span>

### <span data-ttu-id="4af1a-114">1. példa: házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4af1a-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="4af1a-115">Az első parancs megkapja a NewPolicy nevű biztonsági házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4af1a-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="4af1a-116">A második parancs eltávolítja a házirend-objektumot a $Polban.</span><span class="sxs-lookup"><span data-stu-id="4af1a-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="4af1a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4af1a-117">PARAMETERS</span></span>

### <span data-ttu-id="4af1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af1a-118">-DefaultProfile</span></span>
<span data-ttu-id="4af1a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4af1a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af1a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4af1a-120">-Force</span></span>
<span data-ttu-id="4af1a-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4af1a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4af1a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4af1a-122">-Name</span></span>
<span data-ttu-id="4af1a-123">Annak a biztonsági mentési házirendnek a neve, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="4af1a-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="4af1a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4af1a-124">-PassThru</span></span>
<span data-ttu-id="4af1a-125">Adja vissza a házirendet, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="4af1a-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="4af1a-126">-Házirend</span><span class="sxs-lookup"><span data-stu-id="4af1a-126">-Policy</span></span>
<span data-ttu-id="4af1a-127">Az eltávolítandó biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="4af1a-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="4af1a-128">**BackupPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4af1a-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="4af1a-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4af1a-129">-VaultId</span></span>
<span data-ttu-id="4af1a-130">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="4af1a-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4af1a-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4af1a-131">-Confirm</span></span>
<span data-ttu-id="4af1a-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4af1a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4af1a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4af1a-133">-WhatIf</span></span>
<span data-ttu-id="4af1a-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4af1a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4af1a-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4af1a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4af1a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af1a-136">CommonParameters</span></span>
<span data-ttu-id="4af1a-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4af1a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af1a-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af1a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af1a-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4af1a-139">INPUTS</span></span>

### <span data-ttu-id="4af1a-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4af1a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="4af1a-141">Paraméterek: házirend (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4af1a-141">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="4af1a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4af1a-142">System.String</span></span>
<span data-ttu-id="4af1a-143">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4af1a-143">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="4af1a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4af1a-144">OUTPUTS</span></span>

### <span data-ttu-id="4af1a-145">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4af1a-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="4af1a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4af1a-146">NOTES</span></span>

## <span data-ttu-id="4af1a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4af1a-147">RELATED LINKS</span></span>

[<span data-ttu-id="4af1a-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4af1a-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4af1a-149">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4af1a-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4af1a-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4af1a-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


