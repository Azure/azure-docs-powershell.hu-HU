---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 5f3ba7d2bdc573e7a08976e575e86dcf05ae3400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667745"
---
# <span data-ttu-id="834fb-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="834fb-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="834fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="834fb-102">SYNOPSIS</span></span>
<span data-ttu-id="834fb-103">Egy webkampó eltávolítása automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="834fb-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="834fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="834fb-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="834fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="834fb-105">DESCRIPTION</span></span>
<span data-ttu-id="834fb-106">A **Remove-AzAutomationWebhook** parancsmag egy webkampót távolít el egy Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="834fb-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="834fb-107">A rendszer törli a webkampót.</span><span class="sxs-lookup"><span data-stu-id="834fb-107">The webhook is deleted.</span></span>

## <span data-ttu-id="834fb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="834fb-108">EXAMPLES</span></span>

### <span data-ttu-id="834fb-109">Példa 1: webhook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="834fb-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="834fb-110">Ez a parancs eltávolítja a Webhook11 nevű webkampót a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="834fb-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="834fb-111">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="834fb-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="834fb-112">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="834fb-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="834fb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="834fb-113">PARAMETERS</span></span>

### <span data-ttu-id="834fb-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="834fb-114">-AutomationAccountName</span></span>
<span data-ttu-id="834fb-115">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a webkampót.</span><span class="sxs-lookup"><span data-stu-id="834fb-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="834fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="834fb-116">-DefaultProfile</span></span>
<span data-ttu-id="834fb-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="834fb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="834fb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="834fb-118">-Name</span></span>
<span data-ttu-id="834fb-119">Itt adhatja meg annak a webkampónak a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="834fb-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="834fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="834fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="834fb-121">Annak az erőforráscsoport a neve, amelyhez a parancsmag eltávolítja a webkampót.</span><span class="sxs-lookup"><span data-stu-id="834fb-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="834fb-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="834fb-122">-Confirm</span></span>
<span data-ttu-id="834fb-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="834fb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="834fb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="834fb-124">-WhatIf</span></span>
<span data-ttu-id="834fb-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="834fb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="834fb-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="834fb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="834fb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="834fb-127">CommonParameters</span></span>
<span data-ttu-id="834fb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="834fb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="834fb-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="834fb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="834fb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="834fb-130">INPUTS</span></span>

### <span data-ttu-id="834fb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="834fb-131">System.String</span></span>

## <span data-ttu-id="834fb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="834fb-132">OUTPUTS</span></span>

### <span data-ttu-id="834fb-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="834fb-133">System.Void</span></span>

## <span data-ttu-id="834fb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="834fb-134">NOTES</span></span>

## <span data-ttu-id="834fb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="834fb-135">RELATED LINKS</span></span>

[<span data-ttu-id="834fb-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="834fb-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="834fb-137">Új – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="834fb-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="834fb-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="834fb-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


