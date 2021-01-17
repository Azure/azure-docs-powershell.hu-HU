---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478621"
---
# <span data-ttu-id="f2582-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="f2582-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="f2582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2582-102">SYNOPSIS</span></span>
<span data-ttu-id="f2582-103">Az automatizálási fiók regisztrációs kulcsait újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="f2582-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="f2582-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2582-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2582-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2582-105">DESCRIPTION</span></span>
<span data-ttu-id="f2582-106">A **New-AzAutomationKey** parancsmag újragenerálja az Azure Automation-fiók regisztrációs kulcsait.</span><span class="sxs-lookup"><span data-stu-id="f2582-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="f2582-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2582-107">EXAMPLES</span></span>

### <span data-ttu-id="f2582-108">1. példa: Automatizálási fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="f2582-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="f2582-109">Ez a parancs a ResourceGroup01 nevű erőforráscsoport AutomationAccount01 nevű Azure Automation-fiókjának elsődleges kulcsát újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="f2582-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f2582-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2582-110">PARAMETERS</span></span>

### <span data-ttu-id="f2582-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f2582-111">-AutomationAccountName</span></span>
<span data-ttu-id="f2582-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag újragenerálja a kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="f2582-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="f2582-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2582-113">-DefaultProfile</span></span>
<span data-ttu-id="f2582-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f2582-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2582-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f2582-115">-KeyType</span></span>
<span data-ttu-id="f2582-116">Az ügynök regisztrációs kulcsának típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f2582-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="f2582-117">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="f2582-117">Valid values are:</span></span> 
- <span data-ttu-id="f2582-118">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="f2582-118">Primary</span></span> 
- <span data-ttu-id="f2582-119">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="f2582-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2582-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2582-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2582-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2582-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f2582-122">Ez a parancsmag a paraméter által megadott erőforráscsoport automatizálási fiókja kulcsait újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="f2582-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2582-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2582-123">CommonParameters</span></span>
<span data-ttu-id="f2582-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2582-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2582-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2582-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2582-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2582-126">INPUTS</span></span>

### <span data-ttu-id="f2582-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f2582-127">System.String</span></span>

## <span data-ttu-id="f2582-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2582-128">OUTPUTS</span></span>

### <span data-ttu-id="f2582-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="f2582-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="f2582-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2582-130">NOTES</span></span>

## <span data-ttu-id="f2582-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2582-131">RELATED LINKS</span></span>
