---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: e695495b13cbad32cbf1d945a7de4080a88cc49c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505843"
---
# <span data-ttu-id="ba555-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ba555-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="ba555-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba555-102">SYNOPSIS</span></span>
<span data-ttu-id="ba555-103">Automatizálási webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="ba555-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba555-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba555-104">SYNTAX</span></span>

### <span data-ttu-id="ba555-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba555-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba555-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ba555-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba555-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="ba555-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba555-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba555-108">DESCRIPTION</span></span>
<span data-ttu-id="ba555-109">A **Get-AzureRmAutomationWebhook** parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="ba555-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="ba555-110">Ha konkrét webhorgokat szeretne bekapcsolni, adjon meg egy webhook-nevet, vagy adja meg az Azure Automation runbook nevét, hogy beszerezze az ahhoz kapcsolódó webhorgokat.</span><span class="sxs-lookup"><span data-stu-id="ba555-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="ba555-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ba555-111">EXAMPLES</span></span>

### <span data-ttu-id="ba555-112">Példa 1: a runbook minden webakasztójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ba555-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="ba555-113">Ez a parancs a ResourceGroup01 nevű erőforráscsoport AutomationAccount01 nevű automatizálási fiókjának Runbook03 nevű runbook beilleszti az összes webhorgot.</span><span class="sxs-lookup"><span data-stu-id="ba555-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ba555-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba555-114">PARAMETERS</span></span>

### <span data-ttu-id="ba555-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba555-115">-AutomationAccountName</span></span>
<span data-ttu-id="ba555-116">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag webhorogot kap.</span><span class="sxs-lookup"><span data-stu-id="ba555-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="ba555-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba555-117">-DefaultProfile</span></span>
<span data-ttu-id="ba555-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba555-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba555-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba555-119">-Name</span></span>
<span data-ttu-id="ba555-120">Itt adhatja meg annak a webkampónak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="ba555-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba555-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba555-121">-ResourceGroupName</span></span>
<span data-ttu-id="ba555-122">Annak az erőforráscsoportnek a neve, amelyhez a parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="ba555-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="ba555-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="ba555-123">-RunbookName</span></span>
<span data-ttu-id="ba555-124">Annak a runbook a nevét adja meg, amelyhez a parancsmag webhorgokat kap.</span><span class="sxs-lookup"><span data-stu-id="ba555-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba555-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba555-125">CommonParameters</span></span>
<span data-ttu-id="ba555-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba555-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba555-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba555-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba555-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba555-128">INPUTS</span></span>

### <span data-ttu-id="ba555-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="ba555-129">None</span></span>
<span data-ttu-id="ba555-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ba555-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba555-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba555-131">OUTPUTS</span></span>

### <span data-ttu-id="ba555-132">Microsoft. Azure. Command. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="ba555-132">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="ba555-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba555-133">NOTES</span></span>

## <span data-ttu-id="ba555-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba555-134">RELATED LINKS</span></span>

[<span data-ttu-id="ba555-135">Új – AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ba555-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ba555-136">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ba555-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ba555-137">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ba555-137">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


