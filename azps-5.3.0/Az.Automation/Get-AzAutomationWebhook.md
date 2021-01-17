---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478654"
---
# <span data-ttu-id="6a924-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a924-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="6a924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a924-102">SYNOPSIS</span></span>
<span data-ttu-id="6a924-103">Webhookokat kap az automatizálástól.</span><span class="sxs-lookup"><span data-stu-id="6a924-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="6a924-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a924-104">SYNTAX</span></span>

### <span data-ttu-id="6a924-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a924-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a924-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6a924-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a924-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="6a924-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a924-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a924-108">DESCRIPTION</span></span>
<span data-ttu-id="6a924-109">A **Get-AzAutomationWebhook** parancsmag webhooks lesz.</span><span class="sxs-lookup"><span data-stu-id="6a924-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="6a924-110">Adott webhookok lekérte, ha megad egy webhook nevet, vagy egy Azure Automation-runbook nevét, hogy a webhookok csatlakoztatva vannak hozzá.</span><span class="sxs-lookup"><span data-stu-id="6a924-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="6a924-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a924-111">EXAMPLES</span></span>

### <span data-ttu-id="6a924-112">1. példa: Az összes webhook lekérte egy runbookhoz</span><span class="sxs-lookup"><span data-stu-id="6a924-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6a924-113">Ez a parancs a Runbook03 nevű runbook összes webhookját megkapja az AutomationAccount01 nevű automatizálási fiókban az ResourceGroup01 nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6a924-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6a924-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a924-114">PARAMETERS</span></span>

### <span data-ttu-id="6a924-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6a924-115">-AutomationAccountName</span></span>
<span data-ttu-id="6a924-116">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag webhookot kap.</span><span class="sxs-lookup"><span data-stu-id="6a924-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="6a924-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a924-117">-DefaultProfile</span></span>
<span data-ttu-id="6a924-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a924-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a924-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6a924-119">-Name</span></span>
<span data-ttu-id="6a924-120">Annak a webhooknak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="6a924-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6a924-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a924-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a924-122">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja webhookokat kap.</span><span class="sxs-lookup"><span data-stu-id="6a924-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="6a924-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6a924-123">-RunbookName</span></span>
<span data-ttu-id="6a924-124">Annak a runbooknak a nevét adja meg, amelynek a parancsmagja webhookokat kap.</span><span class="sxs-lookup"><span data-stu-id="6a924-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="6a924-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a924-125">CommonParameters</span></span>
<span data-ttu-id="6a924-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a924-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a924-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a924-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a924-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a924-128">INPUTS</span></span>

### <span data-ttu-id="6a924-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6a924-129">System.String</span></span>

## <span data-ttu-id="6a924-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a924-130">OUTPUTS</span></span>

### <span data-ttu-id="6a924-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="6a924-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="6a924-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a924-132">NOTES</span></span>

## <span data-ttu-id="6a924-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a924-133">RELATED LINKS</span></span>

[<span data-ttu-id="6a924-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a924-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="6a924-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a924-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="6a924-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a924-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


