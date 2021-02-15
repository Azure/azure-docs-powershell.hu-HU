---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160090"
---
# <span data-ttu-id="62a85-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="62a85-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="62a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62a85-102">SYNOPSIS</span></span>
<span data-ttu-id="62a85-103">Egy helyreállítási szolgáltatás tárolóját törli.</span><span class="sxs-lookup"><span data-stu-id="62a85-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="62a85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62a85-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a85-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62a85-105">DESCRIPTION</span></span>
<span data-ttu-id="62a85-106">A **Remove-AzRecoveryServicesVault** parancsmag törli a helyreállítási szolgáltatások tárolóját.</span><span class="sxs-lookup"><span data-stu-id="62a85-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="62a85-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62a85-107">EXAMPLES</span></span>

### <span data-ttu-id="62a85-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="62a85-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="62a85-109">Egy helyreállítási szolgáltatás tárolóját törli.</span><span class="sxs-lookup"><span data-stu-id="62a85-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="62a85-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62a85-110">PARAMETERS</span></span>

### <span data-ttu-id="62a85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a85-111">-DefaultProfile</span></span>
<span data-ttu-id="62a85-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62a85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62a85-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="62a85-113">-Vault</span></span>
<span data-ttu-id="62a85-114">Egy Azure Site Recovery tárolóobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="62a85-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="62a85-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62a85-115">-Confirm</span></span>
<span data-ttu-id="62a85-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62a85-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a85-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a85-117">-WhatIf</span></span>
<span data-ttu-id="62a85-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62a85-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62a85-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62a85-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a85-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a85-120">CommonParameters</span></span>
<span data-ttu-id="62a85-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a85-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a85-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62a85-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a85-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62a85-123">INPUTS</span></span>

### <span data-ttu-id="62a85-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="62a85-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="62a85-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62a85-125">OUTPUTS</span></span>

### <span data-ttu-id="62a85-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="62a85-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="62a85-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62a85-127">NOTES</span></span>

## <span data-ttu-id="62a85-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62a85-128">RELATED LINKS</span></span>

[<span data-ttu-id="62a85-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="62a85-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="62a85-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="62a85-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="62a85-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="62a85-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


