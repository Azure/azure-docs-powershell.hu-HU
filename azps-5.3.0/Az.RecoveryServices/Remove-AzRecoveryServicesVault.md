---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468637"
---
# <span data-ttu-id="4ec49-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ec49-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="4ec49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec49-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec49-103">Egy helyreállítási szolgáltatás tárolóját törli.</span><span class="sxs-lookup"><span data-stu-id="4ec49-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="4ec49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ec49-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec49-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ec49-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec49-106">A **Remove-AzRecoveryServicesVault** parancsmag törli a helyreállítási szolgáltatások tárolóját.</span><span class="sxs-lookup"><span data-stu-id="4ec49-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="4ec49-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ec49-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec49-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4ec49-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="4ec49-109">Egy helyreállítási szolgáltatás tárolóját törli.</span><span class="sxs-lookup"><span data-stu-id="4ec49-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="4ec49-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ec49-110">PARAMETERS</span></span>

### <span data-ttu-id="4ec49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec49-111">-DefaultProfile</span></span>
<span data-ttu-id="4ec49-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ec49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ec49-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="4ec49-113">-Vault</span></span>
<span data-ttu-id="4ec49-114">Egy Azure Site Recovery tárolóobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4ec49-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="4ec49-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ec49-115">-Confirm</span></span>
<span data-ttu-id="4ec49-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ec49-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec49-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec49-117">-WhatIf</span></span>
<span data-ttu-id="4ec49-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4ec49-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ec49-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ec49-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec49-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec49-120">CommonParameters</span></span>
<span data-ttu-id="4ec49-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec49-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec49-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ec49-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec49-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ec49-123">INPUTS</span></span>

### <span data-ttu-id="4ec49-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="4ec49-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4ec49-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ec49-125">OUTPUTS</span></span>

### <span data-ttu-id="4ec49-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="4ec49-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="4ec49-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ec49-127">NOTES</span></span>

## <span data-ttu-id="4ec49-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ec49-128">RELATED LINKS</span></span>

[<span data-ttu-id="4ec49-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ec49-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="4ec49-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4ec49-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4ec49-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ec49-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


