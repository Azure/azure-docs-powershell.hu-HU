---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 00125a7ad3d74d3e710b782d0be7fdb20004ef4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014117"
---
# <span data-ttu-id="77945-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="77945-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="77945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77945-102">SYNOPSIS</span></span>
<span data-ttu-id="77945-103">Webhookokat kap az automatizálástól.</span><span class="sxs-lookup"><span data-stu-id="77945-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="77945-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77945-104">SYNTAX</span></span>

### <span data-ttu-id="77945-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77945-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77945-106">ByName</span><span class="sxs-lookup"><span data-stu-id="77945-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77945-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="77945-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77945-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77945-108">DESCRIPTION</span></span>
<span data-ttu-id="77945-109">A **Get-AzAutomationWebhook** parancsmag webhooks lesz.</span><span class="sxs-lookup"><span data-stu-id="77945-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="77945-110">Adott webhookok lekérte, ha megad egy webhook nevet, vagy egy Azure Automation-runbook nevét, hogy a webhookok csatlakoztatva vannak hozzá.</span><span class="sxs-lookup"><span data-stu-id="77945-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span><br>
<span data-ttu-id="77945-111">**Megjegyzés:** A WebhookUri karakterláncot a rendszer biztonsági okokból üres karakterláncként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="77945-111">**Note:** The WebhookUri is returned as empty string due to security concerns.</span></span> <span data-ttu-id="77945-112">Mentse a **New-AzAutomationWebhook** parancsmag által visszaadott webhook URL-címet, mert nem lehet lekérni a **Get-AzAutomationWebhook parancsmag** használatával.</span><span class="sxs-lookup"><span data-stu-id="77945-112">Please make sure to save the webhook URL that **New-AzAutomationWebhook** cmdlet returns, because it cannot be retrieved by using **Get-AzAutomationWebhook**.</span></span>

## <span data-ttu-id="77945-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77945-113">EXAMPLES</span></span>

### <span data-ttu-id="77945-114">1. példa: Az összes webhook lekérte egy runbookhoz</span><span class="sxs-lookup"><span data-stu-id="77945-114">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="77945-115">Ez a parancs a Runbook03 nevű runbook összes webhookját megkapja az AutomationAccount01 nevű automatizálási fiókban az ResourceGroup01 nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="77945-115">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="77945-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77945-116">PARAMETERS</span></span>

### <span data-ttu-id="77945-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="77945-117">-AutomationAccountName</span></span>
<span data-ttu-id="77945-118">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag webhookot kap.</span><span class="sxs-lookup"><span data-stu-id="77945-118">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="77945-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77945-119">-DefaultProfile</span></span>
<span data-ttu-id="77945-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="77945-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77945-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77945-121">-Name</span></span>
<span data-ttu-id="77945-122">Annak a webhooknak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="77945-122">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="77945-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77945-123">-ResourceGroupName</span></span>
<span data-ttu-id="77945-124">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja webhookokat kap.</span><span class="sxs-lookup"><span data-stu-id="77945-124">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="77945-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="77945-125">-RunbookName</span></span>
<span data-ttu-id="77945-126">Annak a runbooknak a nevét adja meg, amelynek a parancsmagja webhookokat kap.</span><span class="sxs-lookup"><span data-stu-id="77945-126">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="77945-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77945-127">CommonParameters</span></span>
<span data-ttu-id="77945-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77945-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77945-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77945-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77945-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77945-130">INPUTS</span></span>

### <span data-ttu-id="77945-131">System.String</span><span class="sxs-lookup"><span data-stu-id="77945-131">System.String</span></span>

## <span data-ttu-id="77945-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77945-132">OUTPUTS</span></span>

### <span data-ttu-id="77945-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="77945-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="77945-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77945-134">NOTES</span></span>

## <span data-ttu-id="77945-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77945-135">RELATED LINKS</span></span>

[<span data-ttu-id="77945-136">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="77945-136">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="77945-137">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="77945-137">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="77945-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="77945-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


