---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478698"
---
# <span data-ttu-id="9baed-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9baed-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="9baed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9baed-102">SYNOPSIS</span></span>
<span data-ttu-id="9baed-103">Metaadatokat kap a modulokhoz az Automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="9baed-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="9baed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9baed-104">SYNTAX</span></span>

### <span data-ttu-id="9baed-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9baed-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9baed-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9baed-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9baed-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9baed-107">DESCRIPTION</span></span>
<span data-ttu-id="9baed-108">A **Get-AzAutomationModule** parancsmag metaadatokat kap a modulokhoz az Azure Automationtől.</span><span class="sxs-lookup"><span data-stu-id="9baed-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="9baed-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9baed-109">EXAMPLES</span></span>

### <span data-ttu-id="9baed-110">1. példa: Az összes modul lekérte</span><span class="sxs-lookup"><span data-stu-id="9baed-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9baed-111">Ez a parancs a Contoso17 nevű automatizálási fiók összes modulját beveszi.</span><span class="sxs-lookup"><span data-stu-id="9baed-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9baed-112">2. példa: Modul lekérte</span><span class="sxs-lookup"><span data-stu-id="9baed-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9baed-113">Ez a parancs kap egy ContosoModule nevű modult a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="9baed-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9baed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9baed-114">PARAMETERS</span></span>

### <span data-ttu-id="9baed-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9baed-115">-AutomationAccountName</span></span>
<span data-ttu-id="9baed-116">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="9baed-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="9baed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9baed-117">-DefaultProfile</span></span>
<span data-ttu-id="9baed-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9baed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9baed-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9baed-119">-Name</span></span>
<span data-ttu-id="9baed-120">Annak a modulnak a nevét adja meg, amelyhez a parancsmag metaadatokat kap.</span><span class="sxs-lookup"><span data-stu-id="9baed-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="9baed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9baed-121">-ResourceGroupName</span></span>
<span data-ttu-id="9baed-122">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="9baed-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="9baed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9baed-123">CommonParameters</span></span>
<span data-ttu-id="9baed-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9baed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9baed-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9baed-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9baed-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9baed-126">INPUTS</span></span>

### <span data-ttu-id="9baed-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9baed-127">System.String</span></span>

## <span data-ttu-id="9baed-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9baed-128">OUTPUTS</span></span>

### <span data-ttu-id="9baed-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="9baed-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9baed-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9baed-130">NOTES</span></span>

## <span data-ttu-id="9baed-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9baed-131">RELATED LINKS</span></span>

[<span data-ttu-id="9baed-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9baed-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="9baed-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9baed-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="9baed-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9baed-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


