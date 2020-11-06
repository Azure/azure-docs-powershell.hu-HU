---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 80b03c8ba4bab5968e55dff40633b014a586d450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497924"
---
# <span data-ttu-id="0679d-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0679d-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="0679d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0679d-102">SYNOPSIS</span></span>
<span data-ttu-id="0679d-103">Házirend törlése egy biztonságimásolat-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="0679d-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0679d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0679d-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0679d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0679d-105">DESCRIPTION</span></span>
<span data-ttu-id="0679d-106">A **Remove-AzureRmBackupProtectionPolicy** parancsmag egy Azure Backup-boltozatból töröl egy házirendet.</span><span class="sxs-lookup"><span data-stu-id="0679d-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>

<span data-ttu-id="0679d-107">A biztonsági mentési házirendek törlése előtt a házirendnek nem lehet megfelelő biztonsági mentési elemekkel rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="0679d-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="0679d-108">Mielőtt törli a házirendet, győződjön meg arról, hogy minden társított elemhez társítva van egy másik házirend.</span><span class="sxs-lookup"><span data-stu-id="0679d-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="0679d-109">Ha egy biztonsági elemmel szeretne másik házirendet társítani, használja az Enable-AzureRmBackupProtection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0679d-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="0679d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0679d-110">EXAMPLES</span></span>

### <span data-ttu-id="0679d-111">1. példa: biztonsági mentési házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0679d-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="0679d-112">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0679d-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="0679d-113">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0679d-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="0679d-114">A második parancs adatmegőrzési házirendet hoz létre a napi adatmegőrzést követő 30 napra, majd a $Daily változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0679d-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="0679d-115">A második parancs a **Get-AzureRmBackupProtectionPolicy** parancsmag használatával kapja meg a DailyBackup nevű védelmi házirendet a boltozaton $Vault.</span><span class="sxs-lookup"><span data-stu-id="0679d-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="0679d-116">A parancs átadja a házirendet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="0679d-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="0679d-117">Ez a parancsmag eltávolítja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="0679d-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="0679d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0679d-118">PARAMETERS</span></span>

### <span data-ttu-id="0679d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0679d-119">-Force</span></span>
<span data-ttu-id="0679d-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0679d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0679d-121">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0679d-121">-ProtectionPolicy</span></span>
<span data-ttu-id="0679d-122">A parancsmag által eltávolított védelmi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0679d-122">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="0679d-123">**AzureRmBackupProtectionPolicy** beolvasásához használja az Get-AzureRmBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0679d-123">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0679d-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0679d-124">-Confirm</span></span>
<span data-ttu-id="0679d-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0679d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0679d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0679d-126">-WhatIf</span></span>
<span data-ttu-id="0679d-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0679d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0679d-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0679d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0679d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0679d-129">-DefaultProfile</span></span>
<span data-ttu-id="0679d-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0679d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0679d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0679d-131">CommonParameters</span></span>
<span data-ttu-id="0679d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0679d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0679d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0679d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0679d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0679d-134">INPUTS</span></span>

### <span data-ttu-id="0679d-135">AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0679d-135">AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="0679d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0679d-136">OUTPUTS</span></span>

### <span data-ttu-id="0679d-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="0679d-137">None</span></span>

## <span data-ttu-id="0679d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0679d-138">NOTES</span></span>

## <span data-ttu-id="0679d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0679d-139">RELATED LINKS</span></span>

[<span data-ttu-id="0679d-140">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0679d-140">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="0679d-141">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0679d-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="0679d-142">Új – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0679d-142">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


