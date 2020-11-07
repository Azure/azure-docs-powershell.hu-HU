---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 798e5f37fdeb53030d43f132eae59c94ea855fc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667760"
---
# <span data-ttu-id="1a96f-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a96f-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="1a96f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a96f-102">SYNOPSIS</span></span>
<span data-ttu-id="1a96f-103">Modul eltávolítása az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="1a96f-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="1a96f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a96f-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a96f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a96f-105">DESCRIPTION</span></span>
<span data-ttu-id="1a96f-106">A **Remove-AzAutomationModule** parancsmag automatizálási fiókból távolítja el a modult az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="1a96f-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="1a96f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a96f-107">EXAMPLES</span></span>

### <span data-ttu-id="1a96f-108">1. példa: modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1a96f-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1a96f-109">Ez a parancs eltávolítja a ContosoModule nevű modult a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="1a96f-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1a96f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a96f-110">PARAMETERS</span></span>

### <span data-ttu-id="1a96f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a96f-111">-AutomationAccountName</span></span>
<span data-ttu-id="1a96f-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a modult.</span><span class="sxs-lookup"><span data-stu-id="1a96f-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="1a96f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a96f-113">-DefaultProfile</span></span>
<span data-ttu-id="1a96f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1a96f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a96f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1a96f-115">-Force</span></span>
<span data-ttu-id="1a96f-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="1a96f-116">ps_force</span></span>

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

### <span data-ttu-id="1a96f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1a96f-117">-Name</span></span>
<span data-ttu-id="1a96f-118">Annak a modulnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1a96f-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1a96f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a96f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a96f-120">Annak az erőforráscsoportnek a nevét adja meg, amelyben a parancsmag eltávolítja a modult.</span><span class="sxs-lookup"><span data-stu-id="1a96f-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="1a96f-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1a96f-121">-Confirm</span></span>
<span data-ttu-id="1a96f-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1a96f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a96f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a96f-123">-WhatIf</span></span>
<span data-ttu-id="1a96f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1a96f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a96f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a96f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a96f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a96f-126">CommonParameters</span></span>
<span data-ttu-id="1a96f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a96f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a96f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a96f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a96f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a96f-129">INPUTS</span></span>

### <span data-ttu-id="1a96f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1a96f-130">System.String</span></span>

## <span data-ttu-id="1a96f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a96f-131">OUTPUTS</span></span>

### <span data-ttu-id="1a96f-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="1a96f-132">System.Void</span></span>

## <span data-ttu-id="1a96f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a96f-133">NOTES</span></span>

## <span data-ttu-id="1a96f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a96f-134">RELATED LINKS</span></span>

[<span data-ttu-id="1a96f-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a96f-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="1a96f-136">Új – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a96f-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="1a96f-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a96f-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


