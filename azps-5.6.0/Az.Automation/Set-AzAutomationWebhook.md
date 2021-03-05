---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 200cc0b6312940606bb4e75f576c60928a84b33f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009798"
---
# <span data-ttu-id="39c4f-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39c4f-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="39c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="39c4f-103">Módosítja az automatizálási runbook webhookját.</span><span class="sxs-lookup"><span data-stu-id="39c4f-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="39c4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39c4f-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39c4f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="39c4f-106">A **Set-AzAutomationWebhook** parancsmag módosítja az Azure Automation-runbook webhook parancsmagját.</span><span class="sxs-lookup"><span data-stu-id="39c4f-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="39c4f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="39c4f-108">1. példa: Webhook letiltása</span><span class="sxs-lookup"><span data-stu-id="39c4f-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="39c4f-109">Ez a parancs letiltja a Webhook01 nevű webhookot az AutomationAccount01 nevű Automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="39c4f-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="39c4f-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="39c4f-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="39c4f-111">Ez a parancs beállítja a futtatás értékét a webhook számára, és arra kényszeríti a runbookot, hogy egy Windows nevű hibrid dolgozói csoporton fusson.</span><span class="sxs-lookup"><span data-stu-id="39c4f-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="39c4f-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="39c4f-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="39c4f-113">Ez a parancs frissíti a futtatás értékét a webhook számára, és arra kényszeríti a runbookot, hogy egy Azure runbook-dolgozón fusson.</span><span class="sxs-lookup"><span data-stu-id="39c4f-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="39c4f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39c4f-114">PARAMETERS</span></span>

### <span data-ttu-id="39c4f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="39c4f-115">-AutomationAccountName</span></span>
<span data-ttu-id="39c4f-116">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag módosítja a webhookot.</span><span class="sxs-lookup"><span data-stu-id="39c4f-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="39c4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c4f-117">-DefaultProfile</span></span>
<span data-ttu-id="39c4f-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="39c4f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39c4f-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="39c4f-119">-IsEnabled</span></span>
<span data-ttu-id="39c4f-120">Azt adja meg, hogy engedélyezve van-e a webhook.</span><span class="sxs-lookup"><span data-stu-id="39c4f-120">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39c4f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="39c4f-121">-Name</span></span>
<span data-ttu-id="39c4f-122">Megadja annak a webhooknak a nevét, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="39c4f-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="39c4f-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="39c4f-123">-Parameters</span></span>
<span data-ttu-id="39c4f-124">A kulcs-érték párok szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="39c4f-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="39c4f-125">A kulcs a runbook paraméternevét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="39c4f-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="39c4f-126">Az értékek a runbook paraméterértékei.</span><span class="sxs-lookup"><span data-stu-id="39c4f-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="39c4f-127">Amikor a runbook webhookra válaszul elindul, ezeket a paramétereket a runbooknak továbbadja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="39c4f-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39c4f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c4f-128">-ResourceGroupName</span></span>
<span data-ttu-id="39c4f-129">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja módosítja a webhookot.</span><span class="sxs-lookup"><span data-stu-id="39c4f-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="39c4f-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="39c4f-130">-RunOn</span></span>
<span data-ttu-id="39c4f-131">Annak a hibrid ügynöknek a választható neve, amelynek végre kell hajtania a runbookot</span><span class="sxs-lookup"><span data-stu-id="39c4f-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c4f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c4f-132">CommonParameters</span></span>
<span data-ttu-id="39c4f-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c4f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c4f-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39c4f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c4f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39c4f-135">INPUTS</span></span>

### <span data-ttu-id="39c4f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="39c4f-136">System.String</span></span>

### <span data-ttu-id="39c4f-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="39c4f-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="39c4f-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="39c4f-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="39c4f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39c4f-139">OUTPUTS</span></span>

### <span data-ttu-id="39c4f-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="39c4f-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="39c4f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39c4f-141">NOTES</span></span>

## <span data-ttu-id="39c4f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39c4f-142">RELATED LINKS</span></span>

[<span data-ttu-id="39c4f-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39c4f-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="39c4f-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39c4f-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="39c4f-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39c4f-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


