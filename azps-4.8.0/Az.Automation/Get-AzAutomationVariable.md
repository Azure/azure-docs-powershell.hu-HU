---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024927"
---
# <span data-ttu-id="483f6-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="483f6-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="483f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="483f6-102">SYNOPSIS</span></span>
<span data-ttu-id="483f6-103">Automatizálási változót kap.</span><span class="sxs-lookup"><span data-stu-id="483f6-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="483f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="483f6-104">SYNTAX</span></span>

### <span data-ttu-id="483f6-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="483f6-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="483f6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="483f6-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="483f6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="483f6-107">DESCRIPTION</span></span>
<span data-ttu-id="483f6-108">A **Get-AzAutomationVariable** parancsmag egy vagy több Azure automatizálási változót kap.</span><span class="sxs-lookup"><span data-stu-id="483f6-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="483f6-109">Ha meghatározott változót szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="483f6-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="483f6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="483f6-110">EXAMPLES</span></span>

### <span data-ttu-id="483f6-111">Példa 1: változó beszerzése</span><span class="sxs-lookup"><span data-stu-id="483f6-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="483f6-112">Az első parancs a Variable06 nevű automatizálási változót kapja a Contoso17 nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="483f6-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="483f6-113">A parancs az objektumot a $Variable változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="483f6-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="483f6-114">A második parancs normál képpont jelöléssel hivatkozik $Variable **Value** tulajdonságára.</span><span class="sxs-lookup"><span data-stu-id="483f6-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="483f6-115">A parancs a $value változó értékét tárolja.</span><span class="sxs-lookup"><span data-stu-id="483f6-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="483f6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="483f6-116">PARAMETERS</span></span>

### <span data-ttu-id="483f6-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="483f6-117">-AutomationAccountName</span></span>
<span data-ttu-id="483f6-118">Annak az automatizálási fióknak a neve, amely a parancsmag által beadott változókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="483f6-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="483f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483f6-119">-DefaultProfile</span></span>
<span data-ttu-id="483f6-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="483f6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="483f6-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="483f6-121">-Name</span></span>
<span data-ttu-id="483f6-122">Annak a változónak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="483f6-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="483f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="483f6-124">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag változókat kap.</span><span class="sxs-lookup"><span data-stu-id="483f6-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="483f6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483f6-125">CommonParameters</span></span>
<span data-ttu-id="483f6-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="483f6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483f6-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483f6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483f6-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="483f6-128">INPUTS</span></span>

### <span data-ttu-id="483f6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="483f6-129">System.String</span></span>

## <span data-ttu-id="483f6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="483f6-130">OUTPUTS</span></span>

### <span data-ttu-id="483f6-131">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="483f6-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="483f6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="483f6-132">NOTES</span></span>

## <span data-ttu-id="483f6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="483f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="483f6-134">Új – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="483f6-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="483f6-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="483f6-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="483f6-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="483f6-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


