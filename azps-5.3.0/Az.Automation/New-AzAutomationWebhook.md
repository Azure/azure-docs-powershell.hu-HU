---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478586"
---
# <span data-ttu-id="c5b5f-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c5b5f-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="c5b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b5f-103">Webhookot hoz létre egy automatizálási runbookhoz.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="c5b5f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5b5f-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b5f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="c5b5f-106">A **New-AzAutomationWebhook** parancsmag létrehoz egy webhookot egy Azure Automation-runbookhoz.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="c5b5f-107">Mindenképpen mentse a parancsmag által visszaadott webhook URL-címet, mert az nem szerezhető be újra.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="c5b5f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5b5f-108">EXAMPLES</span></span>

### <span data-ttu-id="c5b5f-109">1. példa: Webhook létrehozása</span><span class="sxs-lookup"><span data-stu-id="c5b5f-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="c5b5f-110">Ez a parancs létrehoz egy Webhook06 nevű webhookot a ContosoRunbook nevű runbookhoz az AutomationAccount01 nevű Automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="c5b5f-111">A parancs a webhookot a $Webhook tárolja.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="c5b5f-112">A webhook engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-112">The webhook is enabled.</span></span>
<span data-ttu-id="c5b5f-113">A webhook a megadott időpontban lejár.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="c5b5f-114">Ez a parancs semmilyen értéket nem ad meg a webhook paraméterekhez.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="c5b5f-115">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c5b5f-116">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="c5b5f-117">2. példa: Webhook létrehozása paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="c5b5f-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="c5b5f-118">Az első parancs létrehozza a paraméterek szótárát, és tárolja őket a $Params változóban.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="c5b5f-119">A második parancs létrehoz egy Webhook11 nevű webhookot a ContosoRunbook nevű runbookhoz az AutomationAccount01 nevű Automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="c5b5f-120">A parancs a webes $Params rendeli hozzá a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="c5b5f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5b5f-121">PARAMETERS</span></span>

### <span data-ttu-id="c5b5f-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c5b5f-122">-AutomationAccountName</span></span>
<span data-ttu-id="c5b5f-123">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag webhookot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="c5b5f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b5f-124">-DefaultProfile</span></span>
<span data-ttu-id="c5b5f-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c5b5f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5b5f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c5b5f-126">-ExpiryTime</span></span>
<span data-ttu-id="c5b5f-127">A webhook **dateTimeOffset** objektumként való lejárati idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c5b5f-128">Megadhat egy karakterláncot vagy **egy DateTime-t,** amely érvényes **DateTimeOffset** formátumra konvertálható.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b5f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c5b5f-129">-Force</span></span>
<span data-ttu-id="c5b5f-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="c5b5f-130">ps_force</span></span>

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

### <span data-ttu-id="c5b5f-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="c5b5f-131">-IsEnabled</span></span>
<span data-ttu-id="c5b5f-132">Azt adja meg, hogy engedélyezve van-e a webhook.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b5f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c5b5f-133">-Name</span></span>
<span data-ttu-id="c5b5f-134">A webhook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="c5b5f-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="c5b5f-135">-Parameters</span></span>
<span data-ttu-id="c5b5f-136">A kulcs-érték párok szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="c5b5f-137">A kulcsok a runbook paraméternevét.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="c5b5f-138">Az értékek a runbook paraméterértékei.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="c5b5f-139">Amikor a runbook webhookra válaszul elindul, ezeket a paramétereket a runbooknak továbbadja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b5f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b5f-140">-ResourceGroupName</span></span>
<span data-ttu-id="c5b5f-141">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja webhookot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="c5b5f-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c5b5f-142">-RunbookName</span></span>
<span data-ttu-id="c5b5f-143">A webhookhoz társítania kell a runbook nevét.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b5f-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="c5b5f-144">-RunOn</span></span>
<span data-ttu-id="c5b5f-145">Annak a hibrid dolgozócsoportnak a választható neve, amelynek végre kell hajtania a runbookot</span><span class="sxs-lookup"><span data-stu-id="c5b5f-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="c5b5f-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5b5f-146">-Confirm</span></span>
<span data-ttu-id="c5b5f-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b5f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b5f-148">-WhatIf</span></span>
<span data-ttu-id="c5b5f-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b5f-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b5f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b5f-151">CommonParameters</span></span>
<span data-ttu-id="c5b5f-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b5f-153">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5b5f-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b5f-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5b5f-154">INPUTS</span></span>

### <span data-ttu-id="c5b5f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="c5b5f-155">System.String</span></span>

### <span data-ttu-id="c5b5f-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5b5f-156">System.Boolean</span></span>

### <span data-ttu-id="c5b5f-157">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c5b5f-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="c5b5f-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5b5f-158">OUTPUTS</span></span>

### <span data-ttu-id="c5b5f-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="c5b5f-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="c5b5f-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5b5f-160">NOTES</span></span>

## <span data-ttu-id="c5b5f-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5b5f-161">RELATED LINKS</span></span>

[<span data-ttu-id="c5b5f-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c5b5f-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="c5b5f-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c5b5f-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="c5b5f-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c5b5f-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


