---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: b4e60e4bbc7196736c0e49c2b294cf6cb984e7b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009861"
---
# <span data-ttu-id="e2dcb-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="e2dcb-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="e2dcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="e2dcb-103">Eltávolít egy Azure Automation-forrásvezérlőt.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="e2dcb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2dcb-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2dcb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="e2dcb-106">A Remove-AzAutomationSourceControl parancsmag eltávolítja a forrásvezérlőt az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="e2dcb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2dcb-107">EXAMPLES</span></span>

### <span data-ttu-id="e2dcb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2dcb-108">Example 1</span></span>
<span data-ttu-id="e2dcb-109">Ez a parancs eltávolítja a VSTSNative nevű automatizálási forrásvezérlőt a devAccount nevű fiókból.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="e2dcb-110">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="e2dcb-111">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="e2dcb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2dcb-112">PARAMETERS</span></span>

### <span data-ttu-id="e2dcb-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e2dcb-113">-AutomationAccountName</span></span>
<span data-ttu-id="e2dcb-114">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-114">The automation account name.</span></span>

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

### <span data-ttu-id="e2dcb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2dcb-115">-DefaultProfile</span></span>
<span data-ttu-id="e2dcb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2dcb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e2dcb-117">-Name</span></span>
<span data-ttu-id="e2dcb-118">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-118">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2dcb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2dcb-119">-PassThru</span></span>
<span data-ttu-id="e2dcb-120">A PassThru egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2dcb-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2dcb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2dcb-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2dcb-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-123">The resource group name.</span></span>

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

### <span data-ttu-id="e2dcb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2dcb-124">-Confirm</span></span>
<span data-ttu-id="e2dcb-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2dcb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2dcb-126">-WhatIf</span></span>
<span data-ttu-id="e2dcb-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2dcb-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2dcb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2dcb-129">CommonParameters</span></span>
<span data-ttu-id="e2dcb-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2dcb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2dcb-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2dcb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2dcb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2dcb-132">INPUTS</span></span>

### <span data-ttu-id="e2dcb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e2dcb-133">System.String</span></span>

## <span data-ttu-id="e2dcb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2dcb-134">OUTPUTS</span></span>

### <span data-ttu-id="e2dcb-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="e2dcb-135">System.Void</span></span>

### <span data-ttu-id="e2dcb-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e2dcb-136">System.Boolean</span></span>

## <span data-ttu-id="e2dcb-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2dcb-137">NOTES</span></span>

## <span data-ttu-id="e2dcb-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2dcb-138">RELATED LINKS</span></span>
