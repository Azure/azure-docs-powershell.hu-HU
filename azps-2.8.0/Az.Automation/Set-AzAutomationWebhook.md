---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667724"
---
# <span data-ttu-id="e19bf-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e19bf-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="e19bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e19bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e19bf-103">Egy webkampót módosított automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="e19bf-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="e19bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e19bf-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e19bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e19bf-105">DESCRIPTION</span></span>
<span data-ttu-id="e19bf-106">A **set-AzAutomationWebhook** parancsmag egy webkampót módosított az Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="e19bf-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="e19bf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e19bf-107">EXAMPLES</span></span>

### <span data-ttu-id="e19bf-108">Példa 1: webhook letiltása</span><span class="sxs-lookup"><span data-stu-id="e19bf-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="e19bf-109">Ez a parancs letiltja a Webhook01 nevű webkampót a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="e19bf-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="e19bf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e19bf-110">PARAMETERS</span></span>

### <span data-ttu-id="e19bf-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e19bf-111">-AutomationAccountName</span></span>
<span data-ttu-id="e19bf-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="e19bf-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e19bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19bf-113">-DefaultProfile</span></span>
<span data-ttu-id="e19bf-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e19bf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e19bf-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e19bf-115">-IsEnabled</span></span>
<span data-ttu-id="e19bf-116">Megadja, hogy engedélyezve van-e a webhook.</span><span class="sxs-lookup"><span data-stu-id="e19bf-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="e19bf-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e19bf-117">-Name</span></span>
<span data-ttu-id="e19bf-118">Itt adhatja meg annak a webkampónak a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="e19bf-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e19bf-119">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="e19bf-119">-Parameters</span></span>
<span data-ttu-id="e19bf-120">A kulcs/érték párok szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e19bf-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e19bf-121">A kulcsok a runbook paraméterek nevei.</span><span class="sxs-lookup"><span data-stu-id="e19bf-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e19bf-122">Az értékek a runbook paraméter értékei.</span><span class="sxs-lookup"><span data-stu-id="e19bf-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e19bf-123">Ha a runbook egy webkampóra válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="e19bf-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="e19bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="e19bf-125">Annak az erőforráscsoport a neve, amelyhez a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="e19bf-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e19bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19bf-126">CommonParameters</span></span>
<span data-ttu-id="e19bf-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e19bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19bf-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e19bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19bf-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e19bf-129">INPUTS</span></span>

### <span data-ttu-id="e19bf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e19bf-130">System.String</span></span>

### <span data-ttu-id="e19bf-131">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e19bf-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e19bf-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="e19bf-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="e19bf-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e19bf-133">OUTPUTS</span></span>

### <span data-ttu-id="e19bf-134">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="e19bf-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e19bf-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e19bf-135">NOTES</span></span>

## <span data-ttu-id="e19bf-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e19bf-136">RELATED LINKS</span></span>

[<span data-ttu-id="e19bf-137">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e19bf-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="e19bf-138">Új – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e19bf-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="e19bf-139">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e19bf-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


