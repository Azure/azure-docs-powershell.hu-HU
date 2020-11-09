---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302147"
---
# <span data-ttu-id="dc7f6-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dc7f6-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="dc7f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="dc7f6-103">Egy webkampó eltávolítása automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="dc7f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc7f6-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc7f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc7f6-105">DESCRIPTION</span></span>
<span data-ttu-id="dc7f6-106">A **Remove-AzAutomationWebhook** parancsmag egy webkampót távolít el egy Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="dc7f6-107">A rendszer törli a webkampót.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-107">The webhook is deleted.</span></span>

## <span data-ttu-id="dc7f6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dc7f6-108">EXAMPLES</span></span>

### <span data-ttu-id="dc7f6-109">Példa 1: webhook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc7f6-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="dc7f6-110">Ez a parancs eltávolítja a Webhook11 nevű webkampót a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="dc7f6-111">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="dc7f6-112">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dc7f6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc7f6-113">PARAMETERS</span></span>

### <span data-ttu-id="dc7f6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc7f6-114">-AutomationAccountName</span></span>
<span data-ttu-id="dc7f6-115">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a webkampót.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="dc7f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc7f6-116">-DefaultProfile</span></span>
<span data-ttu-id="dc7f6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dc7f6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc7f6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc7f6-118">-Name</span></span>
<span data-ttu-id="dc7f6-119">Itt adhatja meg annak a webkampónak a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dc7f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc7f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc7f6-121">Annak az erőforráscsoport a neve, amelyhez a parancsmag eltávolítja a webkampót.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="dc7f6-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc7f6-122">-Confirm</span></span>
<span data-ttu-id="dc7f6-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc7f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc7f6-124">-WhatIf</span></span>
<span data-ttu-id="dc7f6-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc7f6-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc7f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc7f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc7f6-127">CommonParameters</span></span>
<span data-ttu-id="dc7f6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc7f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc7f6-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc7f6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc7f6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc7f6-130">INPUTS</span></span>

### <span data-ttu-id="dc7f6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dc7f6-131">System.String</span></span>

## <span data-ttu-id="dc7f6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc7f6-132">OUTPUTS</span></span>

### <span data-ttu-id="dc7f6-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="dc7f6-133">System.Void</span></span>

## <span data-ttu-id="dc7f6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc7f6-134">NOTES</span></span>

## <span data-ttu-id="dc7f6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc7f6-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc7f6-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dc7f6-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="dc7f6-137">Új – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dc7f6-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="dc7f6-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dc7f6-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


