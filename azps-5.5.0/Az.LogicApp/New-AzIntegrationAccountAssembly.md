---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147595"
---
# <span data-ttu-id="cc3c3-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cc3c3-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="cc3c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3c3-103">Létrehoz egy integrációs fiók szerelvényt.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="cc3c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc3c3-104">SYNTAX</span></span>

### <span data-ttu-id="cc3c3-105">ByIntegrationAccountAndFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc3c3-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="cc3c3-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="cc3c3-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="cc3c3-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="cc3c3-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="cc3c3-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="cc3c3-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="cc3c3-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc3c3-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="cc3c3-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc3c3-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc3c3-114">DESCRIPTION</span></span>
<span data-ttu-id="cc3c3-115">A **Get-AzIntegrationAccountAssembly** parancsmag létrehoz egy új szerelvényt egy integrációs fiókban.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="cc3c3-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc3c3-116">EXAMPLES</span></span>

### <span data-ttu-id="cc3c3-117">1. példa: Új szerelvény létrehozása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="cc3c3-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="cc3c3-118">Létrehoz egy új szerelvényt az "$localAssemblyFilePath" fájl elérési útjában található helyi fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="cc3c3-119">2. példa: Új szerelvény létrehozása bájtadatokkal</span><span class="sxs-lookup"><span data-stu-id="cc3c3-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="cc3c3-120">Létrehoz egy új szerelvényt a "$assemblyContent" bájttömb használatával.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="cc3c3-121">3. példa: Új szerelvény létrehozása tartalomhivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="cc3c3-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="cc3c3-122">Létrehoz egy új szerelvényt a "$assemblyUrl" URL-címen található bájtadatokkal.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="cc3c3-123">Ez a javasolt módszer nagy méretű szerelvények létrehozására.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="cc3c3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc3c3-124">PARAMETERS</span></span>

### <span data-ttu-id="cc3c3-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="cc3c3-125">-AssemblyData</span></span>
<span data-ttu-id="cc3c3-126">Az integrációs fiók szerelvényének bájtadata.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="cc3c3-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="cc3c3-127">-AssemblyFilePath</span></span>
<span data-ttu-id="cc3c3-128">Az integrációs fiók szerelvényfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="cc3c3-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="cc3c3-129">-ContentLink</span></span>
<span data-ttu-id="cc3c3-130">Az integrációs fiók szerelvényi adataira mutató nyilvánosan hozzáférhető hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="cc3c3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3c3-131">-DefaultProfile</span></span>
<span data-ttu-id="cc3c3-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc3c3-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cc3c3-133">-Metadata</span></span>
<span data-ttu-id="cc3c3-134">Az integrációs fiók szerelvényének metaadatai.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="cc3c3-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cc3c3-135">-Name</span></span>
<span data-ttu-id="cc3c3-136">Az integrációs fiók szerelvényének neve.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc3c3-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="cc3c3-137">-ParentName</span></span>
<span data-ttu-id="cc3c3-138">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-138">The integration account name.</span></span>

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

### <span data-ttu-id="cc3c3-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cc3c3-139">-ParentObject</span></span>
<span data-ttu-id="cc3c3-140">Egy integrációs fiókobjektum.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc3c3-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cc3c3-141">-ParentResourceId</span></span>
<span data-ttu-id="cc3c3-142">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="cc3c3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc3c3-143">-ResourceGroupName</span></span>
<span data-ttu-id="cc3c3-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-144">The resource group name.</span></span>

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

### <span data-ttu-id="cc3c3-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc3c3-145">-Confirm</span></span>
<span data-ttu-id="cc3c3-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc3c3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc3c3-147">-WhatIf</span></span>
<span data-ttu-id="cc3c3-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc3c3-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc3c3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3c3-150">CommonParameters</span></span>
<span data-ttu-id="cc3c3-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc3c3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3c3-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc3c3-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3c3-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc3c3-153">INPUTS</span></span>

### <span data-ttu-id="cc3c3-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cc3c3-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="cc3c3-155">System.String</span><span class="sxs-lookup"><span data-stu-id="cc3c3-155">System.String</span></span>

## <span data-ttu-id="cc3c3-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc3c3-156">OUTPUTS</span></span>

### <span data-ttu-id="cc3c3-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cc3c3-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="cc3c3-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc3c3-158">NOTES</span></span>

## <span data-ttu-id="cc3c3-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc3c3-159">RELATED LINKS</span></span>
