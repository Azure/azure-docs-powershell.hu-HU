---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017950"
---
# <span data-ttu-id="4150c-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4150c-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="4150c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4150c-102">SYNOPSIS</span></span>
<span data-ttu-id="4150c-103">Automatizálási webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="4150c-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="4150c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4150c-104">SYNTAX</span></span>

### <span data-ttu-id="4150c-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4150c-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4150c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4150c-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4150c-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="4150c-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4150c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4150c-108">DESCRIPTION</span></span>
<span data-ttu-id="4150c-109">A **Get-AzAutomationWebhook** parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="4150c-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="4150c-110">Ha konkrét webhorgokat szeretne bekapcsolni, adjon meg egy webhook-nevet, vagy adja meg az Azure Automation runbook nevét, hogy beszerezze az ahhoz kapcsolódó webhorgokat.</span><span class="sxs-lookup"><span data-stu-id="4150c-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="4150c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4150c-111">EXAMPLES</span></span>

### <span data-ttu-id="4150c-112">Példa 1: a runbook minden webakasztójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4150c-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4150c-113">Ez a parancs a ResourceGroup01 nevű erőforráscsoport AutomationAccount01 nevű automatizálási fiókjának Runbook03 nevű runbook beilleszti az összes webhorgot.</span><span class="sxs-lookup"><span data-stu-id="4150c-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4150c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4150c-114">PARAMETERS</span></span>

### <span data-ttu-id="4150c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4150c-115">-AutomationAccountName</span></span>
<span data-ttu-id="4150c-116">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag webhorogot kap.</span><span class="sxs-lookup"><span data-stu-id="4150c-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="4150c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4150c-117">-DefaultProfile</span></span>
<span data-ttu-id="4150c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4150c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4150c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4150c-119">-Name</span></span>
<span data-ttu-id="4150c-120">Itt adhatja meg annak a webkampónak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4150c-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4150c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4150c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4150c-122">Annak az erőforráscsoportnek a neve, amelyhez a parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="4150c-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="4150c-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="4150c-123">-RunbookName</span></span>
<span data-ttu-id="4150c-124">Annak a runbook a nevét adja meg, amelyhez a parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="4150c-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="4150c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4150c-125">CommonParameters</span></span>
<span data-ttu-id="4150c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4150c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4150c-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4150c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4150c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4150c-128">INPUTS</span></span>

### <span data-ttu-id="4150c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4150c-129">System.String</span></span>

## <span data-ttu-id="4150c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4150c-130">OUTPUTS</span></span>

### <span data-ttu-id="4150c-131">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="4150c-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="4150c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4150c-132">NOTES</span></span>

## <span data-ttu-id="4150c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4150c-133">RELATED LINKS</span></span>

[<span data-ttu-id="4150c-134">Új – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4150c-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="4150c-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4150c-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="4150c-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4150c-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


