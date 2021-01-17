---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373209"
---
# <span data-ttu-id="00acf-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="00acf-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="00acf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00acf-102">SYNOPSIS</span></span>
<span data-ttu-id="00acf-103">Eltávolít egy Azure Automation-forrásvezérlőt.</span><span class="sxs-lookup"><span data-stu-id="00acf-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="00acf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00acf-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00acf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00acf-105">DESCRIPTION</span></span>
<span data-ttu-id="00acf-106">A Remove-AzAutomationSourceControl parancsmag eltávolítja a forrásvezérlőket az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="00acf-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="00acf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00acf-107">EXAMPLES</span></span>

### <span data-ttu-id="00acf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="00acf-108">Example 1</span></span>
<span data-ttu-id="00acf-109">Ez a parancs eltávolítja a VSTSNative nevű automatizálási forrásvezérlőt a devAccount nevű fiókból.</span><span class="sxs-lookup"><span data-stu-id="00acf-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="00acf-110">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="00acf-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="00acf-111">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00acf-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="00acf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00acf-112">PARAMETERS</span></span>

### <span data-ttu-id="00acf-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00acf-113">-AutomationAccountName</span></span>
<span data-ttu-id="00acf-114">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="00acf-114">The automation account name.</span></span>

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

### <span data-ttu-id="00acf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00acf-115">-DefaultProfile</span></span>
<span data-ttu-id="00acf-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00acf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00acf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="00acf-117">-Name</span></span>
<span data-ttu-id="00acf-118">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="00acf-118">The source control name.</span></span>

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

### <span data-ttu-id="00acf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00acf-119">-PassThru</span></span>
<span data-ttu-id="00acf-120">A PassThru egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="00acf-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00acf-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="00acf-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="00acf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00acf-122">-ResourceGroupName</span></span>
<span data-ttu-id="00acf-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00acf-123">The resource group name.</span></span>

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

### <span data-ttu-id="00acf-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00acf-124">-Confirm</span></span>
<span data-ttu-id="00acf-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="00acf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00acf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00acf-126">-WhatIf</span></span>
<span data-ttu-id="00acf-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="00acf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00acf-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00acf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00acf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00acf-129">CommonParameters</span></span>
<span data-ttu-id="00acf-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00acf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00acf-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00acf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00acf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00acf-132">INPUTS</span></span>

### <span data-ttu-id="00acf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="00acf-133">System.String</span></span>

## <span data-ttu-id="00acf-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00acf-134">OUTPUTS</span></span>

### <span data-ttu-id="00acf-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="00acf-135">System.Void</span></span>

### <span data-ttu-id="00acf-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00acf-136">System.Boolean</span></span>

## <span data-ttu-id="00acf-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00acf-137">NOTES</span></span>

## <span data-ttu-id="00acf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00acf-138">RELATED LINKS</span></span>
