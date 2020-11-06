---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 22dcc7459c0e574e62f3c87745ad6283fd919386
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494747"
---
# <span data-ttu-id="1071c-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1071c-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1071c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1071c-102">SYNOPSIS</span></span>
<span data-ttu-id="1071c-103">Biztonsági mentési házirend törlése egy boltozatról.</span><span class="sxs-lookup"><span data-stu-id="1071c-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1071c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1071c-104">SYNTAX</span></span>

### <span data-ttu-id="1071c-105">Házirendnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1071c-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1071c-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="1071c-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1071c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1071c-107">DESCRIPTION</span></span>
<span data-ttu-id="1071c-108">A **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági házirendeket töröl a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="1071c-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="1071c-109">A biztonsági mentési házirendek törlése előtt a házirendnek nem lehet megfelelő biztonsági mentési elemekkel rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="1071c-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="1071c-110">Mielőtt törli a házirendet, győződjön meg arról, hogy minden társított elemhez társítva van egy másik házirend.</span><span class="sxs-lookup"><span data-stu-id="1071c-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="1071c-111">Ha egy biztonsági elemmel szeretne másik házirendet társítani, használja az Enable-AzureRmRecoveryServicesBackupProtection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1071c-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="1071c-112">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="1071c-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1071c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="1071c-113">EXAMPLES</span></span>

### <span data-ttu-id="1071c-114">1. példa: házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1071c-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="1071c-115">Az első parancs megkapja a NewPolicy nevű biztonsági házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1071c-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="1071c-116">A második parancs eltávolítja a házirend-objektumot a $Polban.</span><span class="sxs-lookup"><span data-stu-id="1071c-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="1071c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1071c-117">PARAMETERS</span></span>

### <span data-ttu-id="1071c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1071c-118">-Force</span></span>
<span data-ttu-id="1071c-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1071c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1071c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1071c-120">-Name</span></span>
<span data-ttu-id="1071c-121">Annak a biztonsági mentési házirendnek a neve, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="1071c-121">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="1071c-122">-Házirend</span><span class="sxs-lookup"><span data-stu-id="1071c-122">-Policy</span></span>
<span data-ttu-id="1071c-123">Az eltávolítandó biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1071c-123">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="1071c-124">**BackupPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1071c-124">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="1071c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1071c-125">-Confirm</span></span>
<span data-ttu-id="1071c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1071c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1071c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1071c-127">-WhatIf</span></span>
<span data-ttu-id="1071c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1071c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1071c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1071c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1071c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1071c-130">-DefaultProfile</span></span>
<span data-ttu-id="1071c-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1071c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1071c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1071c-132">CommonParameters</span></span>
<span data-ttu-id="1071c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1071c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1071c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1071c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1071c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1071c-135">INPUTS</span></span>

### <span data-ttu-id="1071c-136">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1071c-136">PolicyBase</span></span>
<span data-ttu-id="1071c-137">A ' Policy ' paraméter az "PolicyBase" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1071c-137">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="1071c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1071c-138">OUTPUTS</span></span>

## <span data-ttu-id="1071c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1071c-139">NOTES</span></span>

## <span data-ttu-id="1071c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1071c-140">RELATED LINKS</span></span>

[<span data-ttu-id="1071c-141">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1071c-141">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1071c-142">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1071c-142">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1071c-143">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1071c-143">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


