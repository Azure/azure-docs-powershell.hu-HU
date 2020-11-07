---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2ed40d0ee0698c8e0ee8d4a1c443db32c843ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671991"
---
# <span data-ttu-id="6e758-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6e758-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="6e758-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e758-102">SYNOPSIS</span></span>
<span data-ttu-id="6e758-103">Metaadatokat kap a modulokhoz az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="6e758-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e758-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e758-104">SYNTAX</span></span>

### <span data-ttu-id="6e758-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e758-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e758-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6e758-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e758-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e758-107">DESCRIPTION</span></span>
<span data-ttu-id="6e758-108">A **Get-AzureRmAutomationModule** parancsmag metaadatokat kap az Azure automatizálási modulokból.</span><span class="sxs-lookup"><span data-stu-id="6e758-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="6e758-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6e758-109">EXAMPLES</span></span>

### <span data-ttu-id="6e758-110">Példa 1: az összes modul beolvasása</span><span class="sxs-lookup"><span data-stu-id="6e758-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6e758-111">Ez a parancs a Contoso17 nevű automatizálási fiók összes modulját megkapja.</span><span class="sxs-lookup"><span data-stu-id="6e758-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6e758-112">2. példa: modul beszerzése</span><span class="sxs-lookup"><span data-stu-id="6e758-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6e758-113">Ez a parancs egy ContosoModule nevű modult kap a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="6e758-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6e758-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e758-114">PARAMETERS</span></span>

### <span data-ttu-id="6e758-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6e758-115">-AutomationAccountName</span></span>
<span data-ttu-id="6e758-116">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="6e758-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="6e758-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e758-117">-DefaultProfile</span></span>
<span data-ttu-id="6e758-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e758-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e758-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e758-119">-Name</span></span>
<span data-ttu-id="6e758-120">Annak a modulnak a neve, amelyhez a parancsmag metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="6e758-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e758-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e758-121">-ResourceGroupName</span></span>
<span data-ttu-id="6e758-122">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="6e758-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="6e758-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e758-123">CommonParameters</span></span>
<span data-ttu-id="6e758-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e758-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e758-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e758-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e758-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e758-126">INPUTS</span></span>

### <span data-ttu-id="6e758-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6e758-127">System.String</span></span>

## <span data-ttu-id="6e758-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e758-128">OUTPUTS</span></span>

### <span data-ttu-id="6e758-129">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="6e758-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="6e758-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e758-130">NOTES</span></span>

## <span data-ttu-id="6e758-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e758-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e758-132">Új – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6e758-132">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="6e758-133">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6e758-133">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="6e758-134">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6e758-134">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


