---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371278"
---
# <span data-ttu-id="b6239-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="b6239-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="b6239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6239-102">SYNOPSIS</span></span>
<span data-ttu-id="b6239-103">Frissíti egy tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b6239-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="b6239-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6239-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6239-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6239-105">DESCRIPTION</span></span>
<span data-ttu-id="b6239-106">A **Set-AzRecoveryServicesVaultProperty** parancsmag frissíti a helyreállítási szolgáltatások tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b6239-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="b6239-107">Ez a parancsmag az aktuális halmaz művelet után visszaadja a frissített tárolótulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b6239-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="b6239-108">A tároló ezen parancsmagtulajdonságával, például a szoftveres törlés funkcióval bármikor engedélyezhető.</span><span class="sxs-lookup"><span data-stu-id="b6239-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="b6239-109">**A tároló SoftDeleteFeatureState** tulajdonsága csak akkor tiltható le, ha nincsenek regisztrálva tárolók a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="b6239-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="b6239-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6239-110">EXAMPLES</span></span>

### <span data-ttu-id="b6239-111">1. példa: Egy tároló SoftDeleteFeatureState frissítése</span><span class="sxs-lookup"><span data-stu-id="b6239-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="b6239-112">Az első parancs egy tárolóobjektumot kap, majd a $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="b6239-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="b6239-113">A második parancs a tároló SoftDeleteFeatureState tulajdonságát "Engedélyezve" állapotra frissíti.</span><span class="sxs-lookup"><span data-stu-id="b6239-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="b6239-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6239-114">PARAMETERS</span></span>

### <span data-ttu-id="b6239-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6239-115">-DefaultProfile</span></span>
<span data-ttu-id="b6239-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6239-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6239-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="b6239-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="b6239-118">A Helyreállítási szolgáltatások tároló SoftDeleteFeatureState szolgáltatása.</span><span class="sxs-lookup"><span data-stu-id="b6239-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6239-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b6239-119">-VaultId</span></span>
<span data-ttu-id="b6239-120">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b6239-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b6239-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6239-121">-Confirm</span></span>
<span data-ttu-id="b6239-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b6239-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6239-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6239-123">-WhatIf</span></span>
<span data-ttu-id="b6239-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b6239-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="b6239-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6239-125">CommonParameters</span></span>
<span data-ttu-id="b6239-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6239-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6239-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6239-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6239-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6239-128">INPUTS</span></span>

### <span data-ttu-id="b6239-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b6239-129">System.String</span></span>

### <span data-ttu-id="b6239-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="b6239-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="b6239-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6239-131">OUTPUTS</span></span>

### <span data-ttu-id="b6239-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="b6239-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="b6239-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6239-133">NOTES</span></span>

## <span data-ttu-id="b6239-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6239-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6239-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b6239-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="b6239-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="b6239-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


