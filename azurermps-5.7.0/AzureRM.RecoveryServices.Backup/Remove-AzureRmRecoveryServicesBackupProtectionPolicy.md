---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493059"
---
# <span data-ttu-id="7bb01-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7bb01-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="7bb01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7bb01-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb01-103">Biztonsági mentési házirend törlése egy boltozatról.</span><span class="sxs-lookup"><span data-stu-id="7bb01-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bb01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7bb01-104">SYNTAX</span></span>

### <span data-ttu-id="7bb01-105">Házirendnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7bb01-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb01-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="7bb01-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb01-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7bb01-107">DESCRIPTION</span></span>
<span data-ttu-id="7bb01-108">A **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági házirendeket töröl a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="7bb01-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="7bb01-109">A biztonsági mentési házirendek törlése előtt a házirendnek nem lehet megfelelő biztonsági mentési elemekkel rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="7bb01-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="7bb01-110">Mielőtt törli a házirendet, győződjön meg arról, hogy minden társított elemhez társítva van egy másik házirend.</span><span class="sxs-lookup"><span data-stu-id="7bb01-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="7bb01-111">Ha egy biztonsági elemmel szeretne másik házirendet társítani, használja az Enable-AzureRmRecoveryServicesBackupProtection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7bb01-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="7bb01-112">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="7bb01-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7bb01-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7bb01-113">EXAMPLES</span></span>

### <span data-ttu-id="7bb01-114">1. példa: házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7bb01-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="7bb01-115">Az első parancs megkapja a NewPolicy nevű biztonsági házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7bb01-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="7bb01-116">A második parancs eltávolítja a házirend-objektumot a $Polban.</span><span class="sxs-lookup"><span data-stu-id="7bb01-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="7bb01-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7bb01-117">PARAMETERS</span></span>

### <span data-ttu-id="7bb01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb01-118">-DefaultProfile</span></span>
<span data-ttu-id="7bb01-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bb01-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb01-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7bb01-120">-Force</span></span>
<span data-ttu-id="7bb01-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7bb01-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb01-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7bb01-122">-Name</span></span>
<span data-ttu-id="7bb01-123">Annak a biztonsági mentési házirendnek a neve, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="7bb01-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb01-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bb01-124">-PassThru</span></span>
<span data-ttu-id="7bb01-125">Adja vissza a házirendet, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="7bb01-125">Return the policy to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb01-126">-Házirend</span><span class="sxs-lookup"><span data-stu-id="7bb01-126">-Policy</span></span>
<span data-ttu-id="7bb01-127">Az eltávolítandó biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bb01-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="7bb01-128">**BackupPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7bb01-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb01-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7bb01-129">-Confirm</span></span>
<span data-ttu-id="7bb01-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7bb01-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb01-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb01-131">-WhatIf</span></span>
<span data-ttu-id="7bb01-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7bb01-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb01-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bb01-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb01-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb01-134">CommonParameters</span></span>
<span data-ttu-id="7bb01-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7bb01-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb01-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb01-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb01-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bb01-137">INPUTS</span></span>

### <span data-ttu-id="7bb01-138">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="7bb01-138">PolicyBase</span></span>
<span data-ttu-id="7bb01-139">A ' Policy ' paraméter az "PolicyBase" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7bb01-139">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="7bb01-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bb01-140">OUTPUTS</span></span>

## <span data-ttu-id="7bb01-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7bb01-141">NOTES</span></span>

## <span data-ttu-id="7bb01-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bb01-142">RELATED LINKS</span></span>

[<span data-ttu-id="7bb01-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7bb01-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7bb01-144">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7bb01-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7bb01-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7bb01-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


