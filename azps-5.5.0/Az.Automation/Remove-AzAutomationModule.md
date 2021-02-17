---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205479"
---
# <span data-ttu-id="5a0a3-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="5a0a3-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="5a0a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a0a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0a3-103">Eltávolít egy modult az Automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="5a0a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a0a3-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a0a3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a0a3-105">DESCRIPTION</span></span>
<span data-ttu-id="5a0a3-106">A **Remove-AzAutomationModule** parancsmag eltávolít egy modult egy Automatizálási fiókból az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="5a0a3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a0a3-107">EXAMPLES</span></span>

### <span data-ttu-id="5a0a3-108">1. példa: Modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5a0a3-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5a0a3-109">Ez a parancs eltávolítja a ContosoModule nevű modult a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5a0a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a0a3-110">PARAMETERS</span></span>

### <span data-ttu-id="5a0a3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a0a3-111">-AutomationAccountName</span></span>
<span data-ttu-id="5a0a3-112">Annak az automatizálási fióknak a nevét adja meg, amelyből a parancsmag eltávolít egy modult.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0a3-113">-DefaultProfile</span></span>
<span data-ttu-id="5a0a3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5a0a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a0a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5a0a3-115">-Force</span></span>
<span data-ttu-id="5a0a3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="5a0a3-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5a0a3-117">-Name</span></span>
<span data-ttu-id="5a0a3-118">Annak a modulnak a nevét adja meg, amelyből a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a0a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a0a3-120">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag eltávolít egy modult.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a0a3-121">-Confirm</span></span>
<span data-ttu-id="5a0a3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a0a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a0a3-123">-WhatIf</span></span>
<span data-ttu-id="5a0a3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a0a3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a0a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0a3-126">CommonParameters</span></span>
<span data-ttu-id="5a0a3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a0a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0a3-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a0a3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0a3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a0a3-129">INPUTS</span></span>

### <span data-ttu-id="5a0a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5a0a3-130">System.String</span></span>

## <span data-ttu-id="5a0a3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a0a3-131">OUTPUTS</span></span>

### <span data-ttu-id="5a0a3-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="5a0a3-132">System.Void</span></span>

## <span data-ttu-id="5a0a3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a0a3-133">NOTES</span></span>

## <span data-ttu-id="5a0a3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a0a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="5a0a3-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="5a0a3-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="5a0a3-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="5a0a3-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="5a0a3-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="5a0a3-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


