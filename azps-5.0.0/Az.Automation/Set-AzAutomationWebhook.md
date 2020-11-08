---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186117"
---
# <span data-ttu-id="eab86-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eab86-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="eab86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eab86-102">SYNOPSIS</span></span>
<span data-ttu-id="eab86-103">Egy webkampót módosított automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="eab86-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="eab86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eab86-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eab86-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eab86-105">DESCRIPTION</span></span>
<span data-ttu-id="eab86-106">A **set-AzAutomationWebhook** parancsmag egy webkampót módosított az Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="eab86-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="eab86-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eab86-107">EXAMPLES</span></span>

### <span data-ttu-id="eab86-108">Példa 1: webhook letiltása</span><span class="sxs-lookup"><span data-stu-id="eab86-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="eab86-109">Ez a parancs letiltja a Webhook01 nevű webkampót a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="eab86-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="eab86-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="eab86-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="eab86-111">Ez a parancs a webhook-ra vonatkozó futási értéket állítja be, és a runbook a Windows nevű hibrid munkacsoporton futtatja.</span><span class="sxs-lookup"><span data-stu-id="eab86-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="eab86-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="eab86-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="eab86-113">Ez a parancs frissíti a webhook futtatási értékét, és a runbook egy Azure runbook-munkatárson futtatja.</span><span class="sxs-lookup"><span data-stu-id="eab86-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="eab86-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eab86-114">PARAMETERS</span></span>

### <span data-ttu-id="eab86-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eab86-115">-AutomationAccountName</span></span>
<span data-ttu-id="eab86-116">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="eab86-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="eab86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab86-117">-DefaultProfile</span></span>
<span data-ttu-id="eab86-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="eab86-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eab86-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="eab86-119">-IsEnabled</span></span>
<span data-ttu-id="eab86-120">Megadja, hogy engedélyezve van-e a webhook.</span><span class="sxs-lookup"><span data-stu-id="eab86-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="eab86-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eab86-121">-Name</span></span>
<span data-ttu-id="eab86-122">Itt adhatja meg annak a webkampónak a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="eab86-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eab86-123">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="eab86-123">-Parameters</span></span>
<span data-ttu-id="eab86-124">A kulcs/érték párok szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eab86-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="eab86-125">A kulcsok a runbook paraméterek nevei.</span><span class="sxs-lookup"><span data-stu-id="eab86-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="eab86-126">Az értékek a runbook paraméter értékei.</span><span class="sxs-lookup"><span data-stu-id="eab86-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="eab86-127">Ha a runbook egy webkampóra válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="eab86-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="eab86-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eab86-128">-ResourceGroupName</span></span>
<span data-ttu-id="eab86-129">Annak az erőforráscsoport a neve, amelyhez a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="eab86-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="eab86-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="eab86-130">-RunOn</span></span>
<span data-ttu-id="eab86-131">A runbook végrehajtásához szükséges hibrid ügynök tetszőleges neve</span><span class="sxs-lookup"><span data-stu-id="eab86-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="eab86-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab86-132">CommonParameters</span></span>
<span data-ttu-id="eab86-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eab86-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab86-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eab86-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab86-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eab86-135">INPUTS</span></span>

### <span data-ttu-id="eab86-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eab86-136">System.String</span></span>

### <span data-ttu-id="eab86-137">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eab86-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eab86-138">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="eab86-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="eab86-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eab86-139">OUTPUTS</span></span>

### <span data-ttu-id="eab86-140">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="eab86-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="eab86-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eab86-141">NOTES</span></span>

## <span data-ttu-id="eab86-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eab86-142">RELATED LINKS</span></span>

[<span data-ttu-id="eab86-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eab86-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="eab86-144">Új – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eab86-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="eab86-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eab86-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


