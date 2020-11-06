---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1202ecbdaaf07b9ba5704a01449784172204bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493281"
---
# <span data-ttu-id="cd3f6-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="cd3f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3f6-103">Közzétesz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="cd3f6-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd3f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd3f6-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="cd3f6-106">A **Közzététel-AzureRmAutomationRunbook** parancsmag az Azure automatizálás üzemi környezetében használható runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="cd3f6-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="cd3f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="cd3f6-108">Példa 1: runbook közzététele</span><span class="sxs-lookup"><span data-stu-id="cd3f6-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cd3f6-109">Ez a parancs közzéteszi a Runbk01 nevű runbook az Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="cd3f6-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cd3f6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd3f6-110">PARAMETERS</span></span>

### <span data-ttu-id="cd3f6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd3f6-111">-AutomationAccountName</span></span>
<span data-ttu-id="cd3f6-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag közzéteszi a runbook.</span><span class="sxs-lookup"><span data-stu-id="cd3f6-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="cd3f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3f6-113">-DefaultProfile</span></span>
<span data-ttu-id="cd3f6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cd3f6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd3f6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd3f6-115">-Name</span></span>
<span data-ttu-id="cd3f6-116">Annak a runbook a nevét adja meg, amelyet a parancsmag közzétesz.</span><span class="sxs-lookup"><span data-stu-id="cd3f6-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd3f6-118">Annak az erőforráscsoportnak a neve, amelyhez a parancsmag runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="cd3f6-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="cd3f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3f6-119">CommonParameters</span></span>
<span data-ttu-id="cd3f6-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd3f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3f6-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd3f6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3f6-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd3f6-122">INPUTS</span></span>

### <span data-ttu-id="cd3f6-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="cd3f6-123">None</span></span>
<span data-ttu-id="cd3f6-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cd3f6-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd3f6-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd3f6-125">OUTPUTS</span></span>

### <span data-ttu-id="cd3f6-126">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-126">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="cd3f6-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd3f6-127">NOTES</span></span>

## <span data-ttu-id="cd3f6-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd3f6-128">RELATED LINKS</span></span>

[<span data-ttu-id="cd3f6-129">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-129">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd3f6-130">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-130">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd3f6-131">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd3f6-132">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd3f6-133">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd3f6-134">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-134">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd3f6-135">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-135">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd3f6-136">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd3f6-136">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


