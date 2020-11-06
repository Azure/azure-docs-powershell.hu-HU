---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: 5a47676a7c01052f44acba6362bd24eb65e4c05f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502263"
---
# <span data-ttu-id="77828-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="77828-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77828-102">SYNOPSIS</span></span>
<span data-ttu-id="77828-103">Kap egy runbook.</span><span class="sxs-lookup"><span data-stu-id="77828-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77828-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77828-104">SYNTAX</span></span>

### <span data-ttu-id="77828-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77828-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77828-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="77828-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77828-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="77828-107">DESCRIPTION</span></span>
<span data-ttu-id="77828-108">A **Get-AzureRmAutomationRunbook** parancsmag Azure automatizálási runbooks kap.</span><span class="sxs-lookup"><span data-stu-id="77828-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="77828-109">Ha meghatározott runbook szeretne kapni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="77828-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="77828-110">Példák</span><span class="sxs-lookup"><span data-stu-id="77828-110">EXAMPLES</span></span>

### <span data-ttu-id="77828-111">Példa 1: az összes runbooks beolvasása</span><span class="sxs-lookup"><span data-stu-id="77828-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="77828-112">Ez a parancs a Contoso17 nevű Azure automatizálási fiók minden runbooks bekerül.</span><span class="sxs-lookup"><span data-stu-id="77828-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="77828-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77828-113">PARAMETERS</span></span>

### <span data-ttu-id="77828-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="77828-114">-AutomationAccountName</span></span>
<span data-ttu-id="77828-115">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag runbooks válik.</span><span class="sxs-lookup"><span data-stu-id="77828-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="77828-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77828-116">-DefaultProfile</span></span>
<span data-ttu-id="77828-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="77828-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77828-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77828-118">-Name</span></span>
<span data-ttu-id="77828-119">Annak a runbook a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="77828-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="77828-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77828-120">-ResourceGroupName</span></span>
<span data-ttu-id="77828-121">Annak az erőforráscsoportnek a neve, amelyhez a parancsmag runbooks válik.</span><span class="sxs-lookup"><span data-stu-id="77828-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="77828-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77828-122">CommonParameters</span></span>
<span data-ttu-id="77828-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77828-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77828-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77828-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77828-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77828-125">INPUTS</span></span>

### <span data-ttu-id="77828-126">System. String</span><span class="sxs-lookup"><span data-stu-id="77828-126">System.String</span></span>

## <span data-ttu-id="77828-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77828-127">OUTPUTS</span></span>

### <span data-ttu-id="77828-128">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="77828-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="77828-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77828-129">NOTES</span></span>

## <span data-ttu-id="77828-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77828-130">RELATED LINKS</span></span>

[<span data-ttu-id="77828-131">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-131">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="77828-132">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-132">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="77828-133">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="77828-134">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-134">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="77828-135">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-135">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="77828-136">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-136">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="77828-137">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-137">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="77828-138">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="77828-138">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


