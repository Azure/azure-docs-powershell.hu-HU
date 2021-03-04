---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: d1c61a611b3e2a90c1aa0b0cd21eebdff99ed04b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925545"
---
# <span data-ttu-id="44fb9-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="44fb9-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="44fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="44fb9-103">Eltávolítja az integrációs fiók szerelvényét.</span><span class="sxs-lookup"><span data-stu-id="44fb9-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="44fb9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44fb9-104">SYNTAX</span></span>

### <span data-ttu-id="44fb9-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44fb9-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44fb9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="44fb9-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44fb9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="44fb9-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44fb9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44fb9-108">DESCRIPTION</span></span>
<span data-ttu-id="44fb9-109">A **Remove-AzIntegrationAccountAssembly** parancsmag eltávolít egy szerelvényt egy integrációs fiókból.</span><span class="sxs-lookup"><span data-stu-id="44fb9-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="44fb9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44fb9-110">EXAMPLES</span></span>

### <span data-ttu-id="44fb9-111">1. példa: Szerelvény eltávolítása paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="44fb9-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="44fb9-112">Eltávolítja a "sampleAssembly" nevű szerelvényt, amely a "sampleIntegrationAccount" integrációs fiókban található.</span><span class="sxs-lookup"><span data-stu-id="44fb9-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="44fb9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44fb9-113">PARAMETERS</span></span>

### <span data-ttu-id="44fb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fb9-114">-DefaultProfile</span></span>
<span data-ttu-id="44fb9-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44fb9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44fb9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44fb9-116">-InputObject</span></span>
<span data-ttu-id="44fb9-117">Integrációs fiók összeállítása.</span><span class="sxs-lookup"><span data-stu-id="44fb9-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44fb9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="44fb9-118">-Name</span></span>
<span data-ttu-id="44fb9-119">Az integrációs fiók szerelvényének neve.</span><span class="sxs-lookup"><span data-stu-id="44fb9-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fb9-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="44fb9-120">-ParentName</span></span>
<span data-ttu-id="44fb9-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="44fb9-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fb9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44fb9-122">-PassThru</span></span>
<span data-ttu-id="44fb9-123">Adja vissza, hogy a parancs sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="44fb9-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="44fb9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fb9-124">-ResourceGroupName</span></span>
<span data-ttu-id="44fb9-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44fb9-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fb9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44fb9-126">-ResourceId</span></span>
<span data-ttu-id="44fb9-127">Az integrációs fiók szerelvényének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44fb9-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44fb9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44fb9-128">-Confirm</span></span>
<span data-ttu-id="44fb9-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44fb9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44fb9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44fb9-130">-WhatIf</span></span>
<span data-ttu-id="44fb9-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44fb9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44fb9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44fb9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44fb9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fb9-133">CommonParameters</span></span>
<span data-ttu-id="44fb9-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44fb9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fb9-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44fb9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fb9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44fb9-136">INPUTS</span></span>

### <span data-ttu-id="44fb9-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="44fb9-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="44fb9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="44fb9-138">System.String</span></span>

## <span data-ttu-id="44fb9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44fb9-139">OUTPUTS</span></span>

### <span data-ttu-id="44fb9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44fb9-140">System.Boolean</span></span>

## <span data-ttu-id="44fb9-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44fb9-141">NOTES</span></span>

## <span data-ttu-id="44fb9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44fb9-142">RELATED LINKS</span></span>
