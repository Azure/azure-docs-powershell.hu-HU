---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205542"
---
# <span data-ttu-id="ab887-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ab887-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="ab887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab887-102">SYNOPSIS</span></span>
<span data-ttu-id="ab887-103">Eltávolít egy automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="ab887-103">Removes an Automation account.</span></span>

## <span data-ttu-id="ab887-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab887-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab887-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab887-105">DESCRIPTION</span></span>
<span data-ttu-id="ab887-106">A **Remove-AzAutomationAccount** parancsmag eltávolítja az Azure Automation-fiókot egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="ab887-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="ab887-107">Az automatizálási fiókokról további információt a New-AzAutomationAccount parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="ab887-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="ab887-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab887-108">EXAMPLES</span></span>

### <span data-ttu-id="ab887-109">1. példa: Automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ab887-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ab887-110">Ez a parancs felhasználói ellenőrzés kérése nélkül eltávolítja a ContosoAutomationAccount nevű automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="ab887-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="ab887-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab887-111">PARAMETERS</span></span>

### <span data-ttu-id="ab887-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab887-112">-DefaultProfile</span></span>
<span data-ttu-id="ab887-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab887-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab887-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ab887-114">-Force</span></span>
<span data-ttu-id="ab887-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="ab887-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab887-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ab887-116">-Name</span></span>
<span data-ttu-id="ab887-117">Annak az automatizálási fióknak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ab887-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab887-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab887-118">-ResourceGroupName</span></span>
<span data-ttu-id="ab887-119">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolítja az automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="ab887-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="ab887-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab887-120">-Confirm</span></span>
<span data-ttu-id="ab887-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ab887-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab887-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab887-122">-WhatIf</span></span>
<span data-ttu-id="ab887-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ab887-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab887-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab887-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab887-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab887-125">CommonParameters</span></span>
<span data-ttu-id="ab887-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab887-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab887-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab887-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab887-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab887-128">INPUTS</span></span>

### <span data-ttu-id="ab887-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ab887-129">System.String</span></span>

## <span data-ttu-id="ab887-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab887-130">OUTPUTS</span></span>

### <span data-ttu-id="ab887-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ab887-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ab887-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab887-132">NOTES</span></span>

## <span data-ttu-id="ab887-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab887-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab887-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ab887-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="ab887-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ab887-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="ab887-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ab887-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


