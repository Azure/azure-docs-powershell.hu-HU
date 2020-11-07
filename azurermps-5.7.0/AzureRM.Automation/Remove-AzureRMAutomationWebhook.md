---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 465e3ecd3f80b03eecb58309b18c91cd69c0d5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680822"
---
# <span data-ttu-id="aa113-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="aa113-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="aa113-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa113-102">SYNOPSIS</span></span>
<span data-ttu-id="aa113-103">Egy webkampó eltávolítása automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="aa113-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa113-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa113-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa113-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa113-105">DESCRIPTION</span></span>
<span data-ttu-id="aa113-106">A **Remove-AzureRmAutomationWebhook** parancsmag egy webkampót távolít el egy Azure automatizálási runbook.</span><span class="sxs-lookup"><span data-stu-id="aa113-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="aa113-107">A rendszer törli a webkampót.</span><span class="sxs-lookup"><span data-stu-id="aa113-107">The webhook is deleted.</span></span>

## <span data-ttu-id="aa113-108">Példák</span><span class="sxs-lookup"><span data-stu-id="aa113-108">EXAMPLES</span></span>

### <span data-ttu-id="aa113-109">Példa 1: webhook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa113-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="aa113-110">Ez a parancs eltávolítja a Webhook11 nevű webkampót a AutomationAccount01 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="aa113-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="aa113-111">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa113-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="aa113-112">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa113-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="aa113-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa113-113">PARAMETERS</span></span>

### <span data-ttu-id="aa113-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aa113-114">-AutomationAccountName</span></span>
<span data-ttu-id="aa113-115">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a webkampót.</span><span class="sxs-lookup"><span data-stu-id="aa113-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="aa113-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa113-116">-DefaultProfile</span></span>
<span data-ttu-id="aa113-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aa113-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa113-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa113-118">-Name</span></span>
<span data-ttu-id="aa113-119">Itt adhatja meg annak a webkampónak a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="aa113-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa113-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa113-120">-ResourceGroupName</span></span>
<span data-ttu-id="aa113-121">Annak az erőforráscsoport a neve, amelyhez a parancsmag eltávolítja a webkampót.</span><span class="sxs-lookup"><span data-stu-id="aa113-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="aa113-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa113-122">-Confirm</span></span>
<span data-ttu-id="aa113-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa113-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa113-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa113-124">-WhatIf</span></span>
<span data-ttu-id="aa113-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa113-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa113-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa113-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa113-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa113-127">CommonParameters</span></span>
<span data-ttu-id="aa113-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa113-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa113-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa113-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa113-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa113-130">INPUTS</span></span>

### <span data-ttu-id="aa113-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="aa113-131">None</span></span>
<span data-ttu-id="aa113-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="aa113-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa113-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa113-133">OUTPUTS</span></span>

## <span data-ttu-id="aa113-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa113-134">NOTES</span></span>

## <span data-ttu-id="aa113-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa113-135">RELATED LINKS</span></span>

[<span data-ttu-id="aa113-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="aa113-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="aa113-137">Új – AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="aa113-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="aa113-138">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="aa113-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


