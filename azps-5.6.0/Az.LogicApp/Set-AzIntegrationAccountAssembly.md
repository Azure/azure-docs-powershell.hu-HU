---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 74531aa3c5e142cf3c9638f4910c8d45654a20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936778"
---
# <span data-ttu-id="f4743-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4743-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="f4743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4743-102">SYNOPSIS</span></span>
<span data-ttu-id="f4743-103">Módosítja az integrációs fiók szerelvényét.</span><span class="sxs-lookup"><span data-stu-id="f4743-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="f4743-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4743-104">SYNTAX</span></span>

### <span data-ttu-id="f4743-105">ByIntegrationAccountAndFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4743-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4743-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f4743-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4743-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f4743-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4743-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f4743-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4743-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f4743-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4743-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="f4743-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4743-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f4743-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4743-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f4743-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4743-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="f4743-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4743-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4743-114">DESCRIPTION</span></span>
<span data-ttu-id="f4743-115">A **Set-AzIntegrationAccountAssembly** parancsmag módosítja az integrációs fiók szerelvényét.</span><span class="sxs-lookup"><span data-stu-id="f4743-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="f4743-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4743-116">EXAMPLES</span></span>

### <span data-ttu-id="f4743-117">1. példa: Szerelvény módosítása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="f4743-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f4743-118">Módosítja a "sampleAssembly" szerelvényt az "$localAssemblyFilePath" fájl elérési útjában található helyi fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="f4743-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="f4743-119">2. példa: Szerelvény módosítása bájtadatokkal</span><span class="sxs-lookup"><span data-stu-id="f4743-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f4743-120">Módosítja a "sampleAssembly" nevű szerelvényt az "$assemblyContent" bájttömb használatával.</span><span class="sxs-lookup"><span data-stu-id="f4743-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="f4743-121">3. példa: Szerelvény módosítása tartalomhivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="f4743-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f4743-122">Módosítja a "sampleAssembly" nevű szerelvényt az "$assemblyUrl" URL-címen található bájtadatokkal.</span><span class="sxs-lookup"><span data-stu-id="f4743-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="f4743-123">Ez a javasolt módszer nagy méretű szerelvények létrehozására.</span><span class="sxs-lookup"><span data-stu-id="f4743-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="f4743-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4743-124">PARAMETERS</span></span>

### <span data-ttu-id="f4743-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="f4743-125">-AssemblyData</span></span>
<span data-ttu-id="f4743-126">Az integrációs fiók szerelvényének bájtadata.</span><span class="sxs-lookup"><span data-stu-id="f4743-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="f4743-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="f4743-127">-AssemblyFilePath</span></span>
<span data-ttu-id="f4743-128">Az integrációs fiók szerelvényfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f4743-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="f4743-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="f4743-129">-ContentLink</span></span>
<span data-ttu-id="f4743-130">Az integrációs fiók szerelvényi adataira mutató nyilvánosan hozzáférhető hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="f4743-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="f4743-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4743-131">-DefaultProfile</span></span>
<span data-ttu-id="f4743-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4743-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4743-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4743-133">-InputObject</span></span>
<span data-ttu-id="f4743-134">Integrációs fiók összeállítása.</span><span class="sxs-lookup"><span data-stu-id="f4743-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="f4743-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f4743-135">-Metadata</span></span>
<span data-ttu-id="f4743-136">Az integrációs fiók szerelvényének metaadatai.</span><span class="sxs-lookup"><span data-stu-id="f4743-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="f4743-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f4743-137">-Name</span></span>
<span data-ttu-id="f4743-138">Az integrációs fiók szerelvényének neve.</span><span class="sxs-lookup"><span data-stu-id="f4743-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="f4743-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="f4743-139">-ParentName</span></span>
<span data-ttu-id="f4743-140">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f4743-140">The integration account name.</span></span>

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

### <span data-ttu-id="f4743-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4743-141">-ResourceGroupName</span></span>
<span data-ttu-id="f4743-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4743-142">The resource group name.</span></span>

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

### <span data-ttu-id="f4743-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4743-143">-ResourceId</span></span>
<span data-ttu-id="f4743-144">Az integrációs fiók szerelvényének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4743-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="f4743-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4743-145">-Confirm</span></span>
<span data-ttu-id="f4743-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f4743-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4743-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4743-147">-WhatIf</span></span>
<span data-ttu-id="f4743-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f4743-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4743-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4743-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4743-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4743-150">CommonParameters</span></span>
<span data-ttu-id="f4743-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4743-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4743-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4743-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4743-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4743-153">INPUTS</span></span>

### <span data-ttu-id="f4743-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4743-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="f4743-155">System.String</span><span class="sxs-lookup"><span data-stu-id="f4743-155">System.String</span></span>

## <span data-ttu-id="f4743-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4743-156">OUTPUTS</span></span>

### <span data-ttu-id="f4743-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4743-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="f4743-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4743-158">NOTES</span></span>

## <span data-ttu-id="f4743-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4743-159">RELATED LINKS</span></span>
