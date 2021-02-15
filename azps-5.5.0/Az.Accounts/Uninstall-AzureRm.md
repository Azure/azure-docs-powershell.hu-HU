---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167154"
---
# <span data-ttu-id="62f03-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="62f03-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="62f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62f03-102">SYNOPSIS</span></span>
<span data-ttu-id="62f03-103">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="62f03-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="62f03-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62f03-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62f03-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62f03-105">DESCRIPTION</span></span>
<span data-ttu-id="62f03-106">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="62f03-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="62f03-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62f03-107">EXAMPLES</span></span>

### <span data-ttu-id="62f03-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="62f03-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="62f03-109">A parancs futtatásával eltávolítja az összes AzureRm-modult a gépről annak a PowerShell-verziónak a esetében, amelyben a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62f03-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="62f03-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62f03-110">PARAMETERS</span></span>

### <span data-ttu-id="62f03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f03-111">-DefaultProfile</span></span>
<span data-ttu-id="62f03-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62f03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62f03-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62f03-113">-PassThru</span></span>
<span data-ttu-id="62f03-114">A modulok visszaküldési listája eltávolítva, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="62f03-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="62f03-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62f03-115">-Confirm</span></span>
<span data-ttu-id="62f03-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62f03-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62f03-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f03-117">-WhatIf</span></span>
<span data-ttu-id="62f03-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62f03-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f03-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62f03-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62f03-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f03-120">CommonParameters</span></span>
<span data-ttu-id="62f03-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62f03-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f03-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f03-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f03-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62f03-123">INPUTS</span></span>

### <span data-ttu-id="62f03-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="62f03-124">None</span></span>

## <span data-ttu-id="62f03-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62f03-125">OUTPUTS</span></span>

### <span data-ttu-id="62f03-126">System.String</span><span class="sxs-lookup"><span data-stu-id="62f03-126">System.String</span></span>

## <span data-ttu-id="62f03-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62f03-127">NOTES</span></span>

## <span data-ttu-id="62f03-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62f03-128">RELATED LINKS</span></span>
