---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478517"
---
# <span data-ttu-id="190a4-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="190a4-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="190a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="190a4-102">SYNOPSIS</span></span>
<span data-ttu-id="190a4-103">Eltávolít egy Azure Automation-forrásvezérlőt.</span><span class="sxs-lookup"><span data-stu-id="190a4-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="190a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="190a4-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="190a4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="190a4-105">DESCRIPTION</span></span>
<span data-ttu-id="190a4-106">A Remove-AzAutomationSourceControl parancsmag eltávolítja a forrásvezérlőket az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="190a4-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="190a4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="190a4-107">EXAMPLES</span></span>

### <span data-ttu-id="190a4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="190a4-108">Example 1</span></span>
<span data-ttu-id="190a4-109">Ez a parancs eltávolítja a VSTSNative nevű automatizálási forrásvezérlőt a devAccount nevű fiókból.</span><span class="sxs-lookup"><span data-stu-id="190a4-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="190a4-110">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="190a4-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="190a4-111">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="190a4-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="190a4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="190a4-112">PARAMETERS</span></span>

### <span data-ttu-id="190a4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="190a4-113">-AutomationAccountName</span></span>
<span data-ttu-id="190a4-114">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="190a4-114">The automation account name.</span></span>

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

### <span data-ttu-id="190a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190a4-115">-DefaultProfile</span></span>
<span data-ttu-id="190a4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="190a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="190a4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="190a4-117">-Name</span></span>
<span data-ttu-id="190a4-118">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="190a4-118">The source control name.</span></span>

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

### <span data-ttu-id="190a4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="190a4-119">-PassThru</span></span>
<span data-ttu-id="190a4-120">A PassThru egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="190a4-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="190a4-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="190a4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="190a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="190a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="190a4-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="190a4-123">The resource group name.</span></span>

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

### <span data-ttu-id="190a4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="190a4-124">-Confirm</span></span>
<span data-ttu-id="190a4-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="190a4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190a4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190a4-126">-WhatIf</span></span>
<span data-ttu-id="190a4-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="190a4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="190a4-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="190a4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190a4-129">CommonParameters</span></span>
<span data-ttu-id="190a4-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190a4-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190a4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190a4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="190a4-132">INPUTS</span></span>

### <span data-ttu-id="190a4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="190a4-133">System.String</span></span>

## <span data-ttu-id="190a4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="190a4-134">OUTPUTS</span></span>

### <span data-ttu-id="190a4-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="190a4-135">System.Void</span></span>

### <span data-ttu-id="190a4-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="190a4-136">System.Boolean</span></span>

## <span data-ttu-id="190a4-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="190a4-137">NOTES</span></span>

## <span data-ttu-id="190a4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="190a4-138">RELATED LINKS</span></span>
