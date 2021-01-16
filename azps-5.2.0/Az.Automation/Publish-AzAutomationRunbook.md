---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373405"
---
# <span data-ttu-id="327fd-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="327fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="327fd-102">SYNOPSIS</span></span>
<span data-ttu-id="327fd-103">Közzétesz egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="327fd-103">Publishes a runbook.</span></span>

## <span data-ttu-id="327fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="327fd-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="327fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="327fd-105">DESCRIPTION</span></span>
<span data-ttu-id="327fd-106">A **Publish-AzAutomationRunbook** parancsmag közzétesz egy runbookot az Azure Automation éles környezetében való használatra.</span><span class="sxs-lookup"><span data-stu-id="327fd-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="327fd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="327fd-107">EXAMPLES</span></span>

### <span data-ttu-id="327fd-108">1. példa: Runbook közzététele</span><span class="sxs-lookup"><span data-stu-id="327fd-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="327fd-109">Ez a parancs közzéteszi a Runbk01 nevű runbookot a Contoso17 nevű Azure Automation-fiókban.</span><span class="sxs-lookup"><span data-stu-id="327fd-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="327fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="327fd-110">PARAMETERS</span></span>

### <span data-ttu-id="327fd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="327fd-111">-AutomationAccountName</span></span>
<span data-ttu-id="327fd-112">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag közzétesz egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="327fd-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="327fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327fd-113">-DefaultProfile</span></span>
<span data-ttu-id="327fd-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="327fd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="327fd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="327fd-115">-Name</span></span>
<span data-ttu-id="327fd-116">A parancsmag által közzétett runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="327fd-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="327fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="327fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="327fd-118">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja közzétesz egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="327fd-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="327fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327fd-119">CommonParameters</span></span>
<span data-ttu-id="327fd-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="327fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327fd-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="327fd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327fd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="327fd-122">INPUTS</span></span>

### <span data-ttu-id="327fd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="327fd-123">System.String</span></span>

## <span data-ttu-id="327fd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="327fd-124">OUTPUTS</span></span>

### <span data-ttu-id="327fd-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="327fd-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="327fd-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="327fd-126">NOTES</span></span>

## <span data-ttu-id="327fd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="327fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="327fd-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="327fd-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="327fd-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="327fd-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="327fd-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="327fd-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="327fd-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="327fd-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="327fd-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


