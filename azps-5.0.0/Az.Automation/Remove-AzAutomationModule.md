---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303224"
---
# <span data-ttu-id="c4cd1-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c4cd1-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="c4cd1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cd1-103">Modul eltávolítása az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="c4cd1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4cd1-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4cd1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4cd1-105">DESCRIPTION</span></span>
<span data-ttu-id="c4cd1-106">A **Remove-AzAutomationModule** parancsmag automatizálási fiókból távolítja el a modult az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="c4cd1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c4cd1-107">EXAMPLES</span></span>

### <span data-ttu-id="c4cd1-108">1. példa: modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c4cd1-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c4cd1-109">Ez a parancs eltávolítja a ContosoModule nevű modult a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c4cd1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4cd1-110">PARAMETERS</span></span>

### <span data-ttu-id="c4cd1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4cd1-111">-AutomationAccountName</span></span>
<span data-ttu-id="c4cd1-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a modult.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="c4cd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cd1-113">-DefaultProfile</span></span>
<span data-ttu-id="c4cd1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c4cd1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4cd1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c4cd1-115">-Force</span></span>
<span data-ttu-id="c4cd1-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="c4cd1-116">ps_force</span></span>

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

### <span data-ttu-id="c4cd1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4cd1-117">-Name</span></span>
<span data-ttu-id="c4cd1-118">Annak a modulnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c4cd1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4cd1-119">-ResourceGroupName</span></span>
<span data-ttu-id="c4cd1-120">Annak az erőforráscsoportnek a nevét adja meg, amelyben a parancsmag eltávolítja a modult.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="c4cd1-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4cd1-121">-Confirm</span></span>
<span data-ttu-id="c4cd1-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4cd1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4cd1-123">-WhatIf</span></span>
<span data-ttu-id="c4cd1-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4cd1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4cd1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4cd1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cd1-126">CommonParameters</span></span>
<span data-ttu-id="c4cd1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4cd1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cd1-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4cd1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cd1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4cd1-129">INPUTS</span></span>

### <span data-ttu-id="c4cd1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c4cd1-130">System.String</span></span>

## <span data-ttu-id="c4cd1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4cd1-131">OUTPUTS</span></span>

### <span data-ttu-id="c4cd1-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="c4cd1-132">System.Void</span></span>

## <span data-ttu-id="c4cd1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4cd1-133">NOTES</span></span>

## <span data-ttu-id="c4cd1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4cd1-134">RELATED LINKS</span></span>

[<span data-ttu-id="c4cd1-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c4cd1-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="c4cd1-136">Új – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c4cd1-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="c4cd1-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c4cd1-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


