---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010577"
---
# <span data-ttu-id="a5088-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a5088-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="a5088-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5088-102">SYNOPSIS</span></span>
<span data-ttu-id="a5088-103">Automatizálási változó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a5088-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="a5088-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5088-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5088-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5088-105">DESCRIPTION</span></span>
<span data-ttu-id="a5088-106">A **Remove-AzAutomationVariable** parancsmag egy változót távolít el az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="a5088-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="a5088-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5088-107">EXAMPLES</span></span>

### <span data-ttu-id="a5088-108">Példa 1: változó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5088-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a5088-109">Ez a parancs eltávolítja a StringVariable22 nevű változót a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a5088-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="a5088-110">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5088-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a5088-111">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5088-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a5088-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5088-112">PARAMETERS</span></span>

### <span data-ttu-id="a5088-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a5088-113">-AutomationAccountName</span></span>
<span data-ttu-id="a5088-114">Annak az automatizálási fióknak a neve, amely a parancsmag által törölt változót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a5088-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a5088-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5088-115">-DefaultProfile</span></span>
<span data-ttu-id="a5088-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5088-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5088-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5088-117">-Name</span></span>
<span data-ttu-id="a5088-118">A parancsmag által törölt változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5088-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a5088-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5088-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5088-120">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag törli a változót.</span><span class="sxs-lookup"><span data-stu-id="a5088-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="a5088-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5088-121">-Confirm</span></span>
<span data-ttu-id="a5088-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5088-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5088-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5088-123">-WhatIf</span></span>
<span data-ttu-id="a5088-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5088-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5088-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5088-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5088-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5088-126">CommonParameters</span></span>
<span data-ttu-id="a5088-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5088-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5088-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5088-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5088-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5088-129">INPUTS</span></span>

### <span data-ttu-id="a5088-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a5088-130">System.String</span></span>

## <span data-ttu-id="a5088-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5088-131">OUTPUTS</span></span>

### <span data-ttu-id="a5088-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="a5088-132">System.Void</span></span>

## <span data-ttu-id="a5088-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5088-133">NOTES</span></span>

## <span data-ttu-id="a5088-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5088-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5088-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a5088-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="a5088-136">Új – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a5088-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="a5088-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a5088-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


