---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014988"
---
# <span data-ttu-id="eb9cf-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eb9cf-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="eb9cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9cf-103">Automatizálási webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="eb9cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb9cf-104">SYNTAX</span></span>

### <span data-ttu-id="eb9cf-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb9cf-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb9cf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="eb9cf-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb9cf-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="eb9cf-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb9cf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb9cf-108">DESCRIPTION</span></span>
<span data-ttu-id="eb9cf-109">A **Get-AzAutomationWebhook** parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="eb9cf-110">Ha konkrét webhorgokat szeretne bekapcsolni, adjon meg egy webhook-nevet, vagy adja meg az Azure Automation runbook nevét, hogy beszerezze az ahhoz kapcsolódó webhorgokat.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="eb9cf-111">Példák</span><span class="sxs-lookup"><span data-stu-id="eb9cf-111">EXAMPLES</span></span>

### <span data-ttu-id="eb9cf-112">Példa 1: a runbook minden webakasztójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="eb9cf-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="eb9cf-113">Ez a parancs a ResourceGroup01 nevű erőforráscsoport AutomationAccount01 nevű automatizálási fiókjának Runbook03 nevű runbook beilleszti az összes webhorgot.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="eb9cf-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb9cf-114">PARAMETERS</span></span>

### <span data-ttu-id="eb9cf-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb9cf-115">-AutomationAccountName</span></span>
<span data-ttu-id="eb9cf-116">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag webhorogot kap.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="eb9cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9cf-117">-DefaultProfile</span></span>
<span data-ttu-id="eb9cf-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="eb9cf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb9cf-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb9cf-119">-Name</span></span>
<span data-ttu-id="eb9cf-120">Itt adhatja meg annak a webkampónak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9cf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9cf-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb9cf-122">Annak az erőforráscsoportnek a neve, amelyhez a parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="eb9cf-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="eb9cf-123">-RunbookName</span></span>
<span data-ttu-id="eb9cf-124">Annak a runbook a nevét adja meg, amelyhez a parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9cf-125">CommonParameters</span></span>
<span data-ttu-id="eb9cf-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb9cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9cf-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb9cf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9cf-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb9cf-128">INPUTS</span></span>

### <span data-ttu-id="eb9cf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="eb9cf-129">System.String</span></span>

## <span data-ttu-id="eb9cf-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb9cf-130">OUTPUTS</span></span>

### <span data-ttu-id="eb9cf-131">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="eb9cf-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="eb9cf-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb9cf-132">NOTES</span></span>

## <span data-ttu-id="eb9cf-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb9cf-133">RELATED LINKS</span></span>

[<span data-ttu-id="eb9cf-134">Új – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eb9cf-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="eb9cf-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eb9cf-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="eb9cf-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eb9cf-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


