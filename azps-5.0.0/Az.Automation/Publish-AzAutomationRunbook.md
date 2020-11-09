---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299762"
---
# <span data-ttu-id="a865e-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="a865e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a865e-102">SYNOPSIS</span></span>
<span data-ttu-id="a865e-103">Közzétesz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="a865e-103">Publishes a runbook.</span></span>

## <span data-ttu-id="a865e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a865e-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a865e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a865e-105">DESCRIPTION</span></span>
<span data-ttu-id="a865e-106">A **Közzététel-AzAutomationRunbook** parancsmag az Azure automatizálás üzemi környezetében használható runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="a865e-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="a865e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a865e-107">EXAMPLES</span></span>

### <span data-ttu-id="a865e-108">Példa 1: runbook közzététele</span><span class="sxs-lookup"><span data-stu-id="a865e-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a865e-109">Ez a parancs közzéteszi a Runbk01 nevű runbook az Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a865e-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a865e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a865e-110">PARAMETERS</span></span>

### <span data-ttu-id="a865e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a865e-111">-AutomationAccountName</span></span>
<span data-ttu-id="a865e-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag közzéteszi a runbook.</span><span class="sxs-lookup"><span data-stu-id="a865e-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a865e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a865e-113">-DefaultProfile</span></span>
<span data-ttu-id="a865e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a865e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a865e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a865e-115">-Name</span></span>
<span data-ttu-id="a865e-116">Annak a runbook a nevét adja meg, amelyet a parancsmag közzétesz.</span><span class="sxs-lookup"><span data-stu-id="a865e-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="a865e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a865e-117">-ResourceGroupName</span></span>
<span data-ttu-id="a865e-118">Annak az erőforráscsoportnak a neve, amelyhez a parancsmag runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="a865e-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a865e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a865e-119">CommonParameters</span></span>
<span data-ttu-id="a865e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a865e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a865e-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a865e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a865e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a865e-122">INPUTS</span></span>

### <span data-ttu-id="a865e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a865e-123">System.String</span></span>

## <span data-ttu-id="a865e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a865e-124">OUTPUTS</span></span>

### <span data-ttu-id="a865e-125">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="a865e-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a865e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a865e-126">NOTES</span></span>

## <span data-ttu-id="a865e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a865e-127">RELATED LINKS</span></span>

[<span data-ttu-id="a865e-128">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a865e-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="a865e-130">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a865e-131">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a865e-132">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a865e-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="a865e-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a865e-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a865e-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


