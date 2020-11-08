---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195839"
---
# <span data-ttu-id="190dc-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="190dc-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="190dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="190dc-102">SYNOPSIS</span></span>
<span data-ttu-id="190dc-103">Módosítja az integrációs fiók kódösszeállítását.</span><span class="sxs-lookup"><span data-stu-id="190dc-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="190dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="190dc-104">SYNTAX</span></span>

### <span data-ttu-id="190dc-105">ByIntegrationAccountAndFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="190dc-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190dc-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="190dc-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="190dc-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="190dc-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="190dc-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="190dc-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190dc-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="190dc-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190dc-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="190dc-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190dc-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="190dc-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190dc-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="190dc-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190dc-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="190dc-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="190dc-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="190dc-114">DESCRIPTION</span></span>
<span data-ttu-id="190dc-115">A **set-AzIntegrationAccountAssembly** parancsmag módosította az integrációs fiók kódösszeállítását.</span><span class="sxs-lookup"><span data-stu-id="190dc-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="190dc-116">Példák</span><span class="sxs-lookup"><span data-stu-id="190dc-116">EXAMPLES</span></span>

### <span data-ttu-id="190dc-117">Példa 1: kódösszeállítás módosítása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="190dc-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="190dc-118">Módosítja a "sampleAssembly" nevű kódösszeállítást a "$localAssemblyFilePath" fájl elérési útján található fájl elérési útjának helyi fájlja segítségével.</span><span class="sxs-lookup"><span data-stu-id="190dc-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="190dc-119">2. példa: a kódösszeállítás módosítása a byte Data függvénnyel</span><span class="sxs-lookup"><span data-stu-id="190dc-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="190dc-120">Módosította az "sampleAssembly" nevű kódösszeállítást az "$assemblyContent"-ban található bájtos tömb használatával.</span><span class="sxs-lookup"><span data-stu-id="190dc-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="190dc-121">3. példa: kódösszeállítás módosítása a tartalmi hivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="190dc-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="190dc-122">Módosította az "sampleAssembly" nevű kódösszeállítást a "$assemblyUrl" URL-címen található bájtos adatértékek használatával.</span><span class="sxs-lookup"><span data-stu-id="190dc-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="190dc-123">Ez a javasolt módszer nagy méretű összeállítások készítéséhez.</span><span class="sxs-lookup"><span data-stu-id="190dc-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="190dc-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="190dc-124">PARAMETERS</span></span>

### <span data-ttu-id="190dc-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="190dc-125">-AssemblyData</span></span>
<span data-ttu-id="190dc-126">Az integrációs fiók összeszerelési bájtjának adatait.</span><span class="sxs-lookup"><span data-stu-id="190dc-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="190dc-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="190dc-127">-AssemblyFilePath</span></span>
<span data-ttu-id="190dc-128">Az integrációs fiók kódösszeállítás-fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="190dc-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="190dc-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="190dc-129">-ContentLink</span></span>
<span data-ttu-id="190dc-130">Nyilvánosan elérhető hivatkozás az integrációs fiókok összeállítási adatszolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="190dc-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="190dc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190dc-131">-DefaultProfile</span></span>
<span data-ttu-id="190dc-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="190dc-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="190dc-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="190dc-133">-InputObject</span></span>
<span data-ttu-id="190dc-134">Egy integrációs fiók kódösszeállítása.</span><span class="sxs-lookup"><span data-stu-id="190dc-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="190dc-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="190dc-135">-Metadata</span></span>
<span data-ttu-id="190dc-136">Az integrációs fiók kódösszeállításának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="190dc-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="190dc-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="190dc-137">-Name</span></span>
<span data-ttu-id="190dc-138">Az integrációs fiók kódösszeállításának neve.</span><span class="sxs-lookup"><span data-stu-id="190dc-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="190dc-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="190dc-139">-ParentName</span></span>
<span data-ttu-id="190dc-140">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="190dc-140">The integration account name.</span></span>

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

### <span data-ttu-id="190dc-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="190dc-141">-ResourceGroupName</span></span>
<span data-ttu-id="190dc-142">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="190dc-142">The resource group name.</span></span>

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

### <span data-ttu-id="190dc-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="190dc-143">-ResourceId</span></span>
<span data-ttu-id="190dc-144">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="190dc-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="190dc-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="190dc-145">-Confirm</span></span>
<span data-ttu-id="190dc-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="190dc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190dc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190dc-147">-WhatIf</span></span>
<span data-ttu-id="190dc-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="190dc-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="190dc-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="190dc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190dc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190dc-150">CommonParameters</span></span>
<span data-ttu-id="190dc-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="190dc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190dc-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190dc-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190dc-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="190dc-153">INPUTS</span></span>

### <span data-ttu-id="190dc-154">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="190dc-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="190dc-155">System. String</span><span class="sxs-lookup"><span data-stu-id="190dc-155">System.String</span></span>

## <span data-ttu-id="190dc-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="190dc-156">OUTPUTS</span></span>

### <span data-ttu-id="190dc-157">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="190dc-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="190dc-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="190dc-158">NOTES</span></span>

## <span data-ttu-id="190dc-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="190dc-159">RELATED LINKS</span></span>