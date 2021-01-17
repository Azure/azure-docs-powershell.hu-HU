---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478657"
---
# <span data-ttu-id="21827-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="21827-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="21827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21827-102">SYNOPSIS</span></span>
<span data-ttu-id="21827-103">Automatizálási változót kap.</span><span class="sxs-lookup"><span data-stu-id="21827-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="21827-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21827-104">SYNTAX</span></span>

### <span data-ttu-id="21827-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21827-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21827-106">ByName</span><span class="sxs-lookup"><span data-stu-id="21827-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21827-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21827-107">DESCRIPTION</span></span>
<span data-ttu-id="21827-108">A **Get-AzAutomationVariable parancsmag** egy vagy több Azure Automation-változót kap.</span><span class="sxs-lookup"><span data-stu-id="21827-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="21827-109">Egy adott változó lekért értékének megadásához adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="21827-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="21827-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21827-110">EXAMPLES</span></span>

### <span data-ttu-id="21827-111">1. példa: Változó lekért értéke</span><span class="sxs-lookup"><span data-stu-id="21827-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="21827-112">Az első parancs egy Variable06 nevű Automatizálási változót kap a Contoso17 nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="21827-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="21827-113">A parancs az objektumot a $Variable tárolja.</span><span class="sxs-lookup"><span data-stu-id="21827-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="21827-114">A második parancs szabványos pontként való  hivatkozással hivatkozik a $Variable.</span><span class="sxs-lookup"><span data-stu-id="21827-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="21827-115">A parancs az értéket a $value tárolja.</span><span class="sxs-lookup"><span data-stu-id="21827-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="21827-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21827-116">PARAMETERS</span></span>

### <span data-ttu-id="21827-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="21827-117">-AutomationAccountName</span></span>
<span data-ttu-id="21827-118">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által begyakorolt változókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="21827-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="21827-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21827-119">-DefaultProfile</span></span>
<span data-ttu-id="21827-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="21827-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21827-121">-Name</span><span class="sxs-lookup"><span data-stu-id="21827-121">-Name</span></span>
<span data-ttu-id="21827-122">Annak a változónak a nevét adja meg, amelybe a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="21827-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="21827-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21827-123">-ResourceGroupName</span></span>
<span data-ttu-id="21827-124">Azt az erőforráscsoportot adja meg, amelynek a parancsmagja változókat kap.</span><span class="sxs-lookup"><span data-stu-id="21827-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="21827-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21827-125">CommonParameters</span></span>
<span data-ttu-id="21827-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21827-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21827-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21827-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21827-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21827-128">INPUTS</span></span>

### <span data-ttu-id="21827-129">System.String</span><span class="sxs-lookup"><span data-stu-id="21827-129">System.String</span></span>

## <span data-ttu-id="21827-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21827-130">OUTPUTS</span></span>

### <span data-ttu-id="21827-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="21827-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="21827-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21827-132">NOTES</span></span>

## <span data-ttu-id="21827-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21827-133">RELATED LINKS</span></span>

[<span data-ttu-id="21827-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="21827-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="21827-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="21827-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="21827-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="21827-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


