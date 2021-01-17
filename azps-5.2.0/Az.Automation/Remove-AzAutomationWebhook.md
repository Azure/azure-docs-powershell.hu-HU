---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373167"
---
# <span data-ttu-id="7bd2f-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7bd2f-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="7bd2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd2f-103">Eltávolít egy webhookot egy automatizálási runbookból.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="7bd2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7bd2f-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd2f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7bd2f-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd2f-106">A **Remove-AzAutomationWebhook** parancsmag eltávolítja a webhookot az Azure Automation-runbookból.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="7bd2f-107">A webhook törlődik.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-107">The webhook is deleted.</span></span>

## <span data-ttu-id="7bd2f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7bd2f-108">EXAMPLES</span></span>

### <span data-ttu-id="7bd2f-109">1. példa: Webhook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7bd2f-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="7bd2f-110">Ez a parancs eltávolítja a Webhook11 nevű webhookot az AutomationAccount01 nevű Automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="7bd2f-111">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7bd2f-112">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7bd2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bd2f-113">PARAMETERS</span></span>

### <span data-ttu-id="7bd2f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7bd2f-114">-AutomationAccountName</span></span>
<span data-ttu-id="7bd2f-115">Annak az automatizálási fióknak a nevét adja meg, amelyből a parancsmag eltávolítja a webhookot.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7bd2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd2f-116">-DefaultProfile</span></span>
<span data-ttu-id="7bd2f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7bd2f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bd2f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd2f-118">-Name</span></span>
<span data-ttu-id="7bd2f-119">A parancsmag által eltávolított webhook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7bd2f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd2f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7bd2f-121">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolítja a webhookot.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7bd2f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bd2f-122">-Confirm</span></span>
<span data-ttu-id="7bd2f-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd2f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd2f-124">-WhatIf</span></span>
<span data-ttu-id="7bd2f-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd2f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd2f-127">CommonParameters</span></span>
<span data-ttu-id="7bd2f-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd2f-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd2f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd2f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bd2f-130">INPUTS</span></span>

### <span data-ttu-id="7bd2f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7bd2f-131">System.String</span></span>

## <span data-ttu-id="7bd2f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bd2f-132">OUTPUTS</span></span>

### <span data-ttu-id="7bd2f-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="7bd2f-133">System.Void</span></span>

## <span data-ttu-id="7bd2f-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7bd2f-134">NOTES</span></span>

## <span data-ttu-id="7bd2f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bd2f-135">RELATED LINKS</span></span>

[<span data-ttu-id="7bd2f-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7bd2f-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="7bd2f-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7bd2f-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="7bd2f-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7bd2f-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


