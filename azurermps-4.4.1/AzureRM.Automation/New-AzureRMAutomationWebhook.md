---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: f1062f1e827e27ff891f5b2797fcda95e60f3427
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499255"
---
# <span data-ttu-id="947c2-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="947c2-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="947c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="947c2-102">SYNOPSIS</span></span>
<span data-ttu-id="947c2-103">Egy webkampót hoz létre automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="947c2-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="947c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="947c2-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="947c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="947c2-105">DESCRIPTION</span></span>
<span data-ttu-id="947c2-106">A **New-AzureRmAutomationWebhook** parancsmag egy webhorogot hoz létre az Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="947c2-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="947c2-107">Ügyeljen arra, hogy mentse a parancsmag által visszaadott webhook-URL-címet, mert az nem olvasható vissza.</span><span class="sxs-lookup"><span data-stu-id="947c2-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="947c2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="947c2-108">EXAMPLES</span></span>

### <span data-ttu-id="947c2-109">Példa 1: webhook létrehozása</span><span class="sxs-lookup"><span data-stu-id="947c2-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="947c2-110">Ez a parancs létrehoz egy Webhook06 nevű webkampót a AutomationAccount01 nevű automatizálási fiók ContosoRunbook nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="947c2-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="947c2-111">A parancs a $Webhook változóban tárolja a webkampót.</span><span class="sxs-lookup"><span data-stu-id="947c2-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="947c2-112">A webhook engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="947c2-112">The webhook is enabled.</span></span>
<span data-ttu-id="947c2-113">A webhook a megadott időpontban lejár.</span><span class="sxs-lookup"><span data-stu-id="947c2-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="947c2-114">Ez a parancs nem ad értéket a webhook paraméternek.</span><span class="sxs-lookup"><span data-stu-id="947c2-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="947c2-115">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="947c2-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="947c2-116">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="947c2-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="947c2-117">2. példa: webkampó létrehozása paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="947c2-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="947c2-118">Az első parancs létrehozza a paraméterek szótárát, és a $Params változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="947c2-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="947c2-119">A második parancs létrehoz egy Webhook11 nevű webkampót a ContosoRunbook nevű runbook nevű a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="947c2-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="947c2-120">A parancs kiosztja a paramétereket $Params a webhook-hoz.</span><span class="sxs-lookup"><span data-stu-id="947c2-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="947c2-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="947c2-121">PARAMETERS</span></span>

### <span data-ttu-id="947c2-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="947c2-122">-AutomationAccountName</span></span>
<span data-ttu-id="947c2-123">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag webkampót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="947c2-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="947c2-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="947c2-124">-ExpiryTime</span></span>
<span data-ttu-id="947c2-125">A **DateTimeOffset** -objektumhoz a webhook lejárati időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="947c2-125">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="947c2-126">Megadhat egy karakterláncot vagy egy **datetime** értéket, amelyet átalakíthat érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="947c2-126">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="947c2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="947c2-127">-Force</span></span>
<span data-ttu-id="947c2-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="947c2-128">ps_force</span></span>

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

### <span data-ttu-id="947c2-129">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="947c2-129">-IsEnabled</span></span>
<span data-ttu-id="947c2-130">Megadja, hogy engedélyezve van-e a webhook.</span><span class="sxs-lookup"><span data-stu-id="947c2-130">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="947c2-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="947c2-131">-Name</span></span>
<span data-ttu-id="947c2-132">A webkampó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="947c2-132">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="947c2-133">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="947c2-133">-Parameters</span></span>
<span data-ttu-id="947c2-134">A kulcs/érték párok szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="947c2-134">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="947c2-135">A kulcsok a runbook paraméterek nevei.</span><span class="sxs-lookup"><span data-stu-id="947c2-135">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="947c2-136">Az értékek a runbook paraméter értékei.</span><span class="sxs-lookup"><span data-stu-id="947c2-136">The values are the runbook parameter values.</span></span>
<span data-ttu-id="947c2-137">Ha a runbook egy webkampóra válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="947c2-137">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="947c2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="947c2-138">-ResourceGroupName</span></span>
<span data-ttu-id="947c2-139">Annak az erőforráscsoport-csoportnak a neve, amelyhez a parancsmag létrehoz egy webkampót.</span><span class="sxs-lookup"><span data-stu-id="947c2-139">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="947c2-140">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="947c2-140">-RunbookName</span></span>
<span data-ttu-id="947c2-141">A webkampóhoz társítani kívánt runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="947c2-141">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="947c2-142">-RunOn</span><span class="sxs-lookup"><span data-stu-id="947c2-142">-RunOn</span></span>
<span data-ttu-id="947c2-143">A runbook végrehajtásához szükséges hibrid ügynök tetszőleges neve</span><span class="sxs-lookup"><span data-stu-id="947c2-143">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="947c2-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="947c2-144">-Confirm</span></span>
<span data-ttu-id="947c2-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="947c2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="947c2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="947c2-146">-WhatIf</span></span>
<span data-ttu-id="947c2-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="947c2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="947c2-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="947c2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="947c2-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947c2-149">-DefaultProfile</span></span>
<span data-ttu-id="947c2-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="947c2-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947c2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947c2-151">CommonParameters</span></span>
<span data-ttu-id="947c2-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="947c2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947c2-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="947c2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947c2-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="947c2-154">INPUTS</span></span>

## <span data-ttu-id="947c2-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="947c2-155">OUTPUTS</span></span>

### <span data-ttu-id="947c2-156">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="947c2-156">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="947c2-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="947c2-157">NOTES</span></span>

## <span data-ttu-id="947c2-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="947c2-158">RELATED LINKS</span></span>

[<span data-ttu-id="947c2-159">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="947c2-159">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="947c2-160">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="947c2-160">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="947c2-161">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="947c2-161">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


