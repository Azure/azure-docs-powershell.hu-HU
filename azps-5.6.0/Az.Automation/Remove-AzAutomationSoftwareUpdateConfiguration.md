---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 8ddc84e3fac5df9253ffdacb61d4f4c7a5568c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921497"
---
# <span data-ttu-id="a0430-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0430-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a0430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0430-102">SYNOPSIS</span></span>
<span data-ttu-id="a0430-103">Eltávolítja az Azure Automation szoftverfrissítés-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a0430-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="a0430-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0430-104">SYNTAX</span></span>

### <span data-ttu-id="a0430-105">BySucName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0430-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0430-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="a0430-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0430-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0430-107">DESCRIPTION</span></span>
<span data-ttu-id="a0430-108">Ez a parancsmag eltávolított egy Azure Automatizálási szoftverfrissítés-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a0430-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="a0430-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0430-109">EXAMPLES</span></span>

### <span data-ttu-id="a0430-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a0430-110">Example 1</span></span>
<span data-ttu-id="a0430-111">Az alábbi példa bemutatja, hogyan távolítható el a "MyUpdateConfiguration" automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="a0430-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="a0430-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0430-112">PARAMETERS</span></span>

### <span data-ttu-id="a0430-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0430-113">-AutomationAccountName</span></span>
<span data-ttu-id="a0430-114">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a0430-114">The automation account name.</span></span>

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

### <span data-ttu-id="a0430-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0430-115">-DefaultProfile</span></span>
<span data-ttu-id="a0430-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0430-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0430-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a0430-117">-Name</span></span>
<span data-ttu-id="a0430-118">Az eltávolítható szoftverfrissítés-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="a0430-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0430-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0430-119">-PassThru</span></span>
<span data-ttu-id="a0430-120">A PassThru egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="a0430-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a0430-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a0430-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0430-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0430-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0430-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a0430-123">The resource group name.</span></span>

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

### <span data-ttu-id="a0430-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0430-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="a0430-125">Az eltávolítható szoftverfrissítés-konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="a0430-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0430-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0430-126">-Confirm</span></span>
<span data-ttu-id="a0430-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a0430-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0430-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0430-128">-WhatIf</span></span>
<span data-ttu-id="a0430-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a0430-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0430-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0430-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0430-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0430-131">CommonParameters</span></span>
<span data-ttu-id="a0430-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0430-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0430-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0430-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0430-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0430-134">INPUTS</span></span>

### <span data-ttu-id="a0430-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a0430-135">System.String</span></span>

### <span data-ttu-id="a0430-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0430-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a0430-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0430-137">OUTPUTS</span></span>

### <span data-ttu-id="a0430-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="a0430-138">System.Void</span></span>

### <span data-ttu-id="a0430-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0430-139">System.Boolean</span></span>

## <span data-ttu-id="a0430-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0430-140">NOTES</span></span>

## <span data-ttu-id="a0430-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0430-141">RELATED LINKS</span></span>
