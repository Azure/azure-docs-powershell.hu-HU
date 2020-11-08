---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195424"
---
# <span data-ttu-id="43800-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="43800-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43800-102">SYNOPSIS</span></span>
<span data-ttu-id="43800-103">Kap egy runbook.</span><span class="sxs-lookup"><span data-stu-id="43800-103">Gets a runbook.</span></span>

## <span data-ttu-id="43800-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43800-104">SYNTAX</span></span>

### <span data-ttu-id="43800-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43800-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43800-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="43800-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43800-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="43800-107">DESCRIPTION</span></span>
<span data-ttu-id="43800-108">A **Get-AzAutomationRunbook** parancsmag Azure automatizálási runbooks kap.</span><span class="sxs-lookup"><span data-stu-id="43800-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="43800-109">Ha meghatározott runbook szeretne kapni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="43800-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="43800-110">Példák</span><span class="sxs-lookup"><span data-stu-id="43800-110">EXAMPLES</span></span>

### <span data-ttu-id="43800-111">Példa 1: az összes runbooks beolvasása</span><span class="sxs-lookup"><span data-stu-id="43800-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="43800-112">Ez a parancs a Contoso17 nevű Azure automatizálási fiók minden runbooks bekerül.</span><span class="sxs-lookup"><span data-stu-id="43800-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="43800-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43800-113">PARAMETERS</span></span>

### <span data-ttu-id="43800-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43800-114">-AutomationAccountName</span></span>
<span data-ttu-id="43800-115">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag runbooks válik.</span><span class="sxs-lookup"><span data-stu-id="43800-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="43800-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43800-116">-DefaultProfile</span></span>
<span data-ttu-id="43800-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43800-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43800-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43800-118">-Name</span></span>
<span data-ttu-id="43800-119">Annak a runbook a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="43800-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43800-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43800-120">-ResourceGroupName</span></span>
<span data-ttu-id="43800-121">Annak az erőforráscsoportnek a neve, amelyhez a parancsmag runbooks válik.</span><span class="sxs-lookup"><span data-stu-id="43800-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="43800-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43800-122">CommonParameters</span></span>
<span data-ttu-id="43800-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43800-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43800-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43800-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43800-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43800-125">INPUTS</span></span>

### <span data-ttu-id="43800-126">System. String</span><span class="sxs-lookup"><span data-stu-id="43800-126">System.String</span></span>

## <span data-ttu-id="43800-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43800-127">OUTPUTS</span></span>

### <span data-ttu-id="43800-128">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="43800-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="43800-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43800-129">NOTES</span></span>

## <span data-ttu-id="43800-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43800-130">RELATED LINKS</span></span>

[<span data-ttu-id="43800-131">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="43800-132">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="43800-133">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="43800-134">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="43800-135">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="43800-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="43800-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="43800-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43800-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

