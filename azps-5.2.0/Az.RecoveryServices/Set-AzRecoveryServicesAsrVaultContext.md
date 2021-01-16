---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326209"
---
# <span data-ttu-id="bf6a2-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="bf6a2-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="bf6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf6a2-103">Beállítja a Helyreállítási szolgáltatások tárolókörnyezetét, amely az aktuális PowerShell-munkamenet későbbi Azure-webhely-helyreállítási műveleteihez használható.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="bf6a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bf6a2-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf6a2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bf6a2-105">DESCRIPTION</span></span>
<span data-ttu-id="bf6a2-106">A **Set-AzRecoveryServicesAsrVaultContext parancsmag** további műveletekhez beállítja az Azure Site Recovery tároló környezetét.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="bf6a2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bf6a2-107">EXAMPLES</span></span>

### <span data-ttu-id="bf6a2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bf6a2-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="bf6a2-109">A tároló környezetét a megadott Helyreállítási szolgáltatások tárolóra állítja az aktuális PowerShell-munkamenet későbbi Azure-webhely-helyreállítási műveleteihez.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="bf6a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf6a2-110">PARAMETERS</span></span>

### <span data-ttu-id="bf6a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf6a2-111">-DefaultProfile</span></span>
<span data-ttu-id="bf6a2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf6a2-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="bf6a2-113">-Vault</span></span>
<span data-ttu-id="bf6a2-114">A Helyreállítási szolgáltatások tárolóobjektuma, amely megfelel a Helyreállítási szolgáltatások tárolónak.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf6a2-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf6a2-115">-Confirm</span></span>
<span data-ttu-id="bf6a2-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf6a2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf6a2-117">-WhatIf</span></span>
<span data-ttu-id="bf6a2-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf6a2-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf6a2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf6a2-120">CommonParameters</span></span>
<span data-ttu-id="bf6a2-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf6a2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf6a2-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf6a2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf6a2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf6a2-123">INPUTS</span></span>

### <span data-ttu-id="bf6a2-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="bf6a2-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="bf6a2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf6a2-125">OUTPUTS</span></span>

### <span data-ttu-id="bf6a2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="bf6a2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="bf6a2-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bf6a2-127">NOTES</span></span>

## <span data-ttu-id="bf6a2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf6a2-128">RELATED LINKS</span></span>
