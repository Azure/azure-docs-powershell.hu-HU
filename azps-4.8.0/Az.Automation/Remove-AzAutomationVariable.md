---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024913"
---
# <span data-ttu-id="93229-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93229-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="93229-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93229-102">SYNOPSIS</span></span>
<span data-ttu-id="93229-103">Automatizálási változó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="93229-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="93229-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93229-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93229-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93229-105">DESCRIPTION</span></span>
<span data-ttu-id="93229-106">A **Remove-AzAutomationVariable** parancsmag egy változót távolít el az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="93229-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="93229-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93229-107">EXAMPLES</span></span>

### <span data-ttu-id="93229-108">Példa 1: változó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="93229-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="93229-109">Ez a parancs eltávolítja a StringVariable22 nevű változót a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="93229-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="93229-110">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="93229-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="93229-111">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93229-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="93229-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93229-112">PARAMETERS</span></span>

### <span data-ttu-id="93229-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93229-113">-AutomationAccountName</span></span>
<span data-ttu-id="93229-114">Annak az automatizálási fióknak a neve, amely a parancsmag által törölt változót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="93229-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="93229-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93229-115">-DefaultProfile</span></span>
<span data-ttu-id="93229-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="93229-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93229-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93229-117">-Name</span></span>
<span data-ttu-id="93229-118">A parancsmag által törölt változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93229-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="93229-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93229-119">-ResourceGroupName</span></span>
<span data-ttu-id="93229-120">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag törli a változót.</span><span class="sxs-lookup"><span data-stu-id="93229-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="93229-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93229-121">-Confirm</span></span>
<span data-ttu-id="93229-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93229-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93229-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93229-123">-WhatIf</span></span>
<span data-ttu-id="93229-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93229-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93229-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93229-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93229-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93229-126">CommonParameters</span></span>
<span data-ttu-id="93229-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93229-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93229-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93229-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93229-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93229-129">INPUTS</span></span>

### <span data-ttu-id="93229-130">System. String</span><span class="sxs-lookup"><span data-stu-id="93229-130">System.String</span></span>

## <span data-ttu-id="93229-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93229-131">OUTPUTS</span></span>

### <span data-ttu-id="93229-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="93229-132">System.Void</span></span>

## <span data-ttu-id="93229-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93229-133">NOTES</span></span>

## <span data-ttu-id="93229-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93229-134">RELATED LINKS</span></span>

[<span data-ttu-id="93229-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93229-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="93229-136">Új – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93229-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="93229-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93229-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


