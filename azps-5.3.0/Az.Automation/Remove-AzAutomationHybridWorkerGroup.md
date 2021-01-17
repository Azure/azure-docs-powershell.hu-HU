---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478542"
---
# <span data-ttu-id="34c4f-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="34c4f-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="34c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="34c4f-103">Eltávolítja a hibrid dolgozók csoportját az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="34c4f-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="34c4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="34c4f-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34c4f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="34c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="34c4f-106">A Remove-AzAutomationHybridWorkerGroup parancsmag eltávolítja a hibrid dolgozók csoportját az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="34c4f-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="34c4f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="34c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="34c4f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="34c4f-108">Example 1</span></span>
<span data-ttu-id="34c4f-109">Ez a parancs név szerint eltávolítja a hibrid dolgozókat.</span><span class="sxs-lookup"><span data-stu-id="34c4f-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="34c4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="34c4f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34c4f-111">-AutomationAccountName</span></span>
<span data-ttu-id="34c4f-112">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="34c4f-112">The automation account name.</span></span>

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

### <span data-ttu-id="34c4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c4f-113">-DefaultProfile</span></span>
<span data-ttu-id="34c4f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34c4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34c4f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="34c4f-115">-Name</span></span>
<span data-ttu-id="34c4f-116">A hibrid dolgozók csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="34c4f-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c4f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c4f-117">-ResourceGroupName</span></span>
<span data-ttu-id="34c4f-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="34c4f-118">The resource group name.</span></span>

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

### <span data-ttu-id="34c4f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34c4f-119">-Confirm</span></span>
<span data-ttu-id="34c4f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="34c4f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c4f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c4f-121">-WhatIf</span></span>
<span data-ttu-id="34c4f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="34c4f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34c4f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34c4f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c4f-124">CommonParameters</span></span>
<span data-ttu-id="34c4f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c4f-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c4f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c4f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34c4f-127">INPUTS</span></span>

### <span data-ttu-id="34c4f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="34c4f-128">System.String</span></span>

## <span data-ttu-id="34c4f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c4f-129">OUTPUTS</span></span>

### <span data-ttu-id="34c4f-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="34c4f-130">System.Void</span></span>

## <span data-ttu-id="34c4f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="34c4f-131">NOTES</span></span>

## <span data-ttu-id="34c4f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34c4f-132">RELATED LINKS</span></span>
