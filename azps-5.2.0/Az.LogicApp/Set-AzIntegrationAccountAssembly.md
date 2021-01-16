---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343830"
---
# <span data-ttu-id="dd99d-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dd99d-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="dd99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd99d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd99d-103">Módosítja az integrációs fiók szerelvényét.</span><span class="sxs-lookup"><span data-stu-id="dd99d-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="dd99d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd99d-104">SYNTAX</span></span>

### <span data-ttu-id="dd99d-105">ByIntegrationAccountAndFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd99d-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd99d-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="dd99d-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd99d-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="dd99d-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd99d-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="dd99d-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd99d-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="dd99d-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd99d-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="dd99d-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd99d-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="dd99d-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd99d-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="dd99d-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd99d-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="dd99d-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd99d-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd99d-114">DESCRIPTION</span></span>
<span data-ttu-id="dd99d-115">A **Set-AzIntegrationAccountAssembly** parancsmag módosítja az integrációs fiók szerelvényét.</span><span class="sxs-lookup"><span data-stu-id="dd99d-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="dd99d-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd99d-116">EXAMPLES</span></span>

### <span data-ttu-id="dd99d-117">1. példa: Szerelvény módosítása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="dd99d-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="dd99d-118">Módosítja a "sampleAssembly" szerelvényt az "$localAssemblyFilePath" fájl elérési útjában található helyi fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="dd99d-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="dd99d-119">2. példa: Szerelvény módosítása bájtadatokkal</span><span class="sxs-lookup"><span data-stu-id="dd99d-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="dd99d-120">Módosítja a "sampleAssembly" nevű szerelvényt az "$assemblyContent" bájttömb használatával.</span><span class="sxs-lookup"><span data-stu-id="dd99d-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="dd99d-121">3. példa: Szerelvény módosítása tartalomhivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="dd99d-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="dd99d-122">Módosítja a "sampleAssembly" nevű szerelvényt az "$assemblyUrl" URL-címen található bájtadatokkal.</span><span class="sxs-lookup"><span data-stu-id="dd99d-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="dd99d-123">Ez a javasolt módszer nagy méretű szerelvények létrehozására.</span><span class="sxs-lookup"><span data-stu-id="dd99d-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="dd99d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd99d-124">PARAMETERS</span></span>

### <span data-ttu-id="dd99d-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="dd99d-125">-AssemblyData</span></span>
<span data-ttu-id="dd99d-126">Az integrációs fiók szerelvényének bájtadata.</span><span class="sxs-lookup"><span data-stu-id="dd99d-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="dd99d-127">-AssemblyFilePath</span></span>
<span data-ttu-id="dd99d-128">Az integrációs fiók szerelvényfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="dd99d-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="dd99d-129">-ContentLink</span></span>
<span data-ttu-id="dd99d-130">Az integrációs fiók szerelvényi adataira mutató nyilvánosan hozzáférhető hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="dd99d-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd99d-131">-DefaultProfile</span></span>
<span data-ttu-id="dd99d-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd99d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd99d-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd99d-133">-InputObject</span></span>
<span data-ttu-id="dd99d-134">Integrációs fiók összeállítása.</span><span class="sxs-lookup"><span data-stu-id="dd99d-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dd99d-135">-Metadata</span></span>
<span data-ttu-id="dd99d-136">Az integrációs fiók szerelvényének metaadatai.</span><span class="sxs-lookup"><span data-stu-id="dd99d-136">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="dd99d-137">-Name</span></span>
<span data-ttu-id="dd99d-138">Az integrációs fiók szerelvényének neve.</span><span class="sxs-lookup"><span data-stu-id="dd99d-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="dd99d-139">-ParentName</span></span>
<span data-ttu-id="dd99d-140">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="dd99d-140">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd99d-141">-ResourceGroupName</span></span>
<span data-ttu-id="dd99d-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dd99d-142">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd99d-143">-ResourceId</span></span>
<span data-ttu-id="dd99d-144">Az integrációs fiók szerelvényének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd99d-144">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd99d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd99d-145">-Confirm</span></span>
<span data-ttu-id="dd99d-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd99d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd99d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd99d-147">-WhatIf</span></span>
<span data-ttu-id="dd99d-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd99d-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd99d-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd99d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd99d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd99d-150">CommonParameters</span></span>
<span data-ttu-id="dd99d-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd99d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd99d-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd99d-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd99d-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd99d-153">INPUTS</span></span>

### <span data-ttu-id="dd99d-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dd99d-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="dd99d-155">System.String</span><span class="sxs-lookup"><span data-stu-id="dd99d-155">System.String</span></span>

## <span data-ttu-id="dd99d-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd99d-156">OUTPUTS</span></span>

### <span data-ttu-id="dd99d-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dd99d-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="dd99d-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd99d-158">NOTES</span></span>

## <span data-ttu-id="dd99d-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd99d-159">RELATED LINKS</span></span>
