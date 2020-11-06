---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: 47d384c6ca55fb428922dc3d9e59de84aa0db166
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492025"
---
# <span data-ttu-id="946c6-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="946c6-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="946c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="946c6-102">SYNOPSIS</span></span>
<span data-ttu-id="946c6-103">Egy webkampót módosított automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="946c6-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="946c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="946c6-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="946c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="946c6-105">DESCRIPTION</span></span>
<span data-ttu-id="946c6-106">A **set-AzureRmAutomationWebhook** parancsmag egy webkampót módosított az Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="946c6-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="946c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="946c6-107">EXAMPLES</span></span>

### <span data-ttu-id="946c6-108">Példa 1: webhook letiltása</span><span class="sxs-lookup"><span data-stu-id="946c6-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="946c6-109">Ez a parancs letiltja a Webhook01 nevű webkampót a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="946c6-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="946c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="946c6-110">PARAMETERS</span></span>

### <span data-ttu-id="946c6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="946c6-111">-AutomationAccountName</span></span>
<span data-ttu-id="946c6-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="946c6-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="946c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946c6-113">-DefaultProfile</span></span>
<span data-ttu-id="946c6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="946c6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="946c6-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="946c6-115">-IsEnabled</span></span>
<span data-ttu-id="946c6-116">Megadja, hogy engedélyezve van-e a webhook.</span><span class="sxs-lookup"><span data-stu-id="946c6-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="946c6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="946c6-117">-Name</span></span>
<span data-ttu-id="946c6-118">Itt adhatja meg annak a webkampónak a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="946c6-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="946c6-119">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="946c6-119">-Parameters</span></span>
<span data-ttu-id="946c6-120">A kulcs/érték párok szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="946c6-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="946c6-121">A kulcsok a runbook paraméterek nevei.</span><span class="sxs-lookup"><span data-stu-id="946c6-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="946c6-122">Az értékek a runbook paraméter értékei.</span><span class="sxs-lookup"><span data-stu-id="946c6-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="946c6-123">Ha a runbook egy webkampóra válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="946c6-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="946c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="946c6-125">Annak az erőforráscsoport a neve, amelyhez a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="946c6-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="946c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946c6-126">CommonParameters</span></span>
<span data-ttu-id="946c6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="946c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946c6-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946c6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="946c6-129">INPUTS</span></span>

### <span data-ttu-id="946c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="946c6-130">System.String</span></span>

### <span data-ttu-id="946c6-131">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="946c6-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="946c6-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="946c6-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="946c6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="946c6-133">OUTPUTS</span></span>

### <span data-ttu-id="946c6-134">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="946c6-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="946c6-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="946c6-135">NOTES</span></span>

## <span data-ttu-id="946c6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="946c6-136">RELATED LINKS</span></span>

[<span data-ttu-id="946c6-137">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="946c6-137">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="946c6-138">Új – AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="946c6-138">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="946c6-139">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="946c6-139">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


