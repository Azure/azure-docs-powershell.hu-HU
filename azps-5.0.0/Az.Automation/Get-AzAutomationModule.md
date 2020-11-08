---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188139"
---
# <span data-ttu-id="f3307-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f3307-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="f3307-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3307-102">SYNOPSIS</span></span>
<span data-ttu-id="f3307-103">Metaadatokat kap a modulokhoz az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="f3307-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="f3307-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3307-104">SYNTAX</span></span>

### <span data-ttu-id="f3307-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3307-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3307-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f3307-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3307-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3307-107">DESCRIPTION</span></span>
<span data-ttu-id="f3307-108">A **Get-AzAutomationModule** parancsmag metaadatokat kap az Azure automatizálási modulokból.</span><span class="sxs-lookup"><span data-stu-id="f3307-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="f3307-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f3307-109">EXAMPLES</span></span>

### <span data-ttu-id="f3307-110">Példa 1: az összes modul beolvasása</span><span class="sxs-lookup"><span data-stu-id="f3307-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f3307-111">Ez a parancs a Contoso17 nevű automatizálási fiók összes modulját megkapja.</span><span class="sxs-lookup"><span data-stu-id="f3307-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f3307-112">2. példa: modul beszerzése</span><span class="sxs-lookup"><span data-stu-id="f3307-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f3307-113">Ez a parancs egy ContosoModule nevű modult kap a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="f3307-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f3307-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3307-114">PARAMETERS</span></span>

### <span data-ttu-id="f3307-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3307-115">-AutomationAccountName</span></span>
<span data-ttu-id="f3307-116">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="f3307-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="f3307-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3307-117">-DefaultProfile</span></span>
<span data-ttu-id="f3307-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f3307-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3307-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3307-119">-Name</span></span>
<span data-ttu-id="f3307-120">Annak a modulnak a neve, amelyhez a parancsmag metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="f3307-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="f3307-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3307-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3307-122">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="f3307-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="f3307-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3307-123">CommonParameters</span></span>
<span data-ttu-id="f3307-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3307-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3307-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3307-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3307-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3307-126">INPUTS</span></span>

### <span data-ttu-id="f3307-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f3307-127">System.String</span></span>

## <span data-ttu-id="f3307-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3307-128">OUTPUTS</span></span>

### <span data-ttu-id="f3307-129">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="f3307-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="f3307-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3307-130">NOTES</span></span>

## <span data-ttu-id="f3307-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3307-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3307-132">Új – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f3307-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="f3307-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f3307-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="f3307-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f3307-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


