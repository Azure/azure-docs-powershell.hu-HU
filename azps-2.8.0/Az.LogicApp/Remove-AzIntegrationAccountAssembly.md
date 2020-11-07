---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: ce3a3ae24a1064e036bc66e0fa7bfdaa6c74e0c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666034"
---
# <span data-ttu-id="88cf6-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="88cf6-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="88cf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="88cf6-103">Eltávolítja az integrációs fiók kódösszeállítását.</span><span class="sxs-lookup"><span data-stu-id="88cf6-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="88cf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88cf6-104">SYNTAX</span></span>

### <span data-ttu-id="88cf6-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88cf6-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88cf6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="88cf6-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88cf6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="88cf6-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88cf6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="88cf6-108">DESCRIPTION</span></span>
<span data-ttu-id="88cf6-109">A **Remove-AzIntegrationAccountAssembly** parancsmag egy integrációs fiókból távolítja el a kódösszeállítást.</span><span class="sxs-lookup"><span data-stu-id="88cf6-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="88cf6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="88cf6-110">EXAMPLES</span></span>

### <span data-ttu-id="88cf6-111">1. példa: a kódösszeállítás paraméterekből való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="88cf6-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="88cf6-112">Eltávolítja a "sampleAssembly" nevű kódösszeállítást az "sampleIntegrationAccount" integrációs fiókjában.</span><span class="sxs-lookup"><span data-stu-id="88cf6-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="88cf6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88cf6-113">PARAMETERS</span></span>

### <span data-ttu-id="88cf6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88cf6-114">-DefaultProfile</span></span>
<span data-ttu-id="88cf6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88cf6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88cf6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88cf6-116">-InputObject</span></span>
<span data-ttu-id="88cf6-117">Egy integrációs fiók kódösszeállítása.</span><span class="sxs-lookup"><span data-stu-id="88cf6-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="88cf6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88cf6-118">-Name</span></span>
<span data-ttu-id="88cf6-119">Az integrációs fiók kódösszeállításának neve.</span><span class="sxs-lookup"><span data-stu-id="88cf6-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="88cf6-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="88cf6-120">-ParentName</span></span>
<span data-ttu-id="88cf6-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="88cf6-121">The integration account name.</span></span>

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

### <span data-ttu-id="88cf6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88cf6-122">-PassThru</span></span>
<span data-ttu-id="88cf6-123">Adja meg, hogy a parancs sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="88cf6-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="88cf6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88cf6-124">-ResourceGroupName</span></span>
<span data-ttu-id="88cf6-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="88cf6-125">The resource group name.</span></span>

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

### <span data-ttu-id="88cf6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88cf6-126">-ResourceId</span></span>
<span data-ttu-id="88cf6-127">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="88cf6-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="88cf6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88cf6-128">-Confirm</span></span>
<span data-ttu-id="88cf6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88cf6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88cf6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88cf6-130">-WhatIf</span></span>
<span data-ttu-id="88cf6-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88cf6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88cf6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88cf6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88cf6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88cf6-133">CommonParameters</span></span>
<span data-ttu-id="88cf6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88cf6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88cf6-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88cf6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88cf6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88cf6-136">INPUTS</span></span>

### <span data-ttu-id="88cf6-137">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="88cf6-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="88cf6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="88cf6-138">System.String</span></span>

## <span data-ttu-id="88cf6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88cf6-139">OUTPUTS</span></span>

### <span data-ttu-id="88cf6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88cf6-140">System.Boolean</span></span>

## <span data-ttu-id="88cf6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88cf6-141">NOTES</span></span>

## <span data-ttu-id="88cf6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88cf6-142">RELATED LINKS</span></span>
