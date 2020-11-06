---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: d0443d5c15dec1324a5fe306ddec7303426449b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499080"
---
# <span data-ttu-id="ab348-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ab348-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="ab348-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab348-102">SYNOPSIS</span></span>
<span data-ttu-id="ab348-103">Egy webkampót módosított automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="ab348-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab348-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab348-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab348-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab348-105">DESCRIPTION</span></span>
<span data-ttu-id="ab348-106">A **set-AzureRmAutomationWebhook** parancsmag egy webkampót módosított az Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="ab348-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="ab348-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ab348-107">EXAMPLES</span></span>

### <span data-ttu-id="ab348-108">Példa 1: webhook letiltása</span><span class="sxs-lookup"><span data-stu-id="ab348-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="ab348-109">Ez a parancs letiltja a Webhook01 nevű webkampót a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="ab348-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="ab348-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab348-110">PARAMETERS</span></span>

### <span data-ttu-id="ab348-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ab348-111">-AutomationAccountName</span></span>
<span data-ttu-id="ab348-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="ab348-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab348-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab348-113">-DefaultProfile</span></span>
<span data-ttu-id="ab348-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab348-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab348-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="ab348-115">-IsEnabled</span></span>
<span data-ttu-id="ab348-116">Megadja, hogy engedélyezve van-e a webhook.</span><span class="sxs-lookup"><span data-stu-id="ab348-116">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab348-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab348-117">-Name</span></span>
<span data-ttu-id="ab348-118">Itt adhatja meg annak a webkampónak a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="ab348-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab348-119">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="ab348-119">-Parameters</span></span>
<span data-ttu-id="ab348-120">A kulcs/érték párok szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab348-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="ab348-121">A kulcsok a runbook paraméterek nevei.</span><span class="sxs-lookup"><span data-stu-id="ab348-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="ab348-122">Az értékek a runbook paraméter értékei.</span><span class="sxs-lookup"><span data-stu-id="ab348-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="ab348-123">Ha a runbook egy webkampóra válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="ab348-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab348-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab348-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab348-125">Annak az erőforráscsoport a neve, amelyhez a parancsmag egy webkampót módosít.</span><span class="sxs-lookup"><span data-stu-id="ab348-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab348-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab348-126">CommonParameters</span></span>
<span data-ttu-id="ab348-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab348-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab348-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab348-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab348-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab348-129">INPUTS</span></span>

### <span data-ttu-id="ab348-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab348-130">None</span></span>
<span data-ttu-id="ab348-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ab348-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab348-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab348-132">OUTPUTS</span></span>

### <span data-ttu-id="ab348-133">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="ab348-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="ab348-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab348-134">NOTES</span></span>

## <span data-ttu-id="ab348-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab348-135">RELATED LINKS</span></span>

[<span data-ttu-id="ab348-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ab348-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ab348-137">Új – AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ab348-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ab348-138">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ab348-138">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


