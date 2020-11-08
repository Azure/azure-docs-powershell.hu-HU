---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002890"
---
# <span data-ttu-id="77a60-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="77a60-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="77a60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77a60-102">SYNOPSIS</span></span>
<span data-ttu-id="77a60-103">Módosítja az integrációs fiók kódösszeállítását.</span><span class="sxs-lookup"><span data-stu-id="77a60-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="77a60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77a60-104">SYNTAX</span></span>

### <span data-ttu-id="77a60-105">ByIntegrationAccountAndFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77a60-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a60-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="77a60-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77a60-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="77a60-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77a60-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="77a60-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a60-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="77a60-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a60-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="77a60-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a60-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="77a60-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a60-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="77a60-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a60-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="77a60-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77a60-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="77a60-114">DESCRIPTION</span></span>
<span data-ttu-id="77a60-115">A **set-AzIntegrationAccountAssembly** parancsmag módosította az integrációs fiók kódösszeállítását.</span><span class="sxs-lookup"><span data-stu-id="77a60-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="77a60-116">Példák</span><span class="sxs-lookup"><span data-stu-id="77a60-116">EXAMPLES</span></span>

### <span data-ttu-id="77a60-117">Példa 1: kódösszeállítás módosítása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="77a60-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="77a60-118">Módosítja a "sampleAssembly" nevű kódösszeállítást a "$localAssemblyFilePath" fájl elérési útján található fájl elérési útjának helyi fájlja segítségével.</span><span class="sxs-lookup"><span data-stu-id="77a60-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="77a60-119">2. példa: a kódösszeállítás módosítása a byte Data függvénnyel</span><span class="sxs-lookup"><span data-stu-id="77a60-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="77a60-120">Módosította az "sampleAssembly" nevű kódösszeállítást az "$assemblyContent"-ban található bájtos tömb használatával.</span><span class="sxs-lookup"><span data-stu-id="77a60-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="77a60-121">3. példa: kódösszeállítás módosítása a tartalmi hivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="77a60-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="77a60-122">Módosította az "sampleAssembly" nevű kódösszeállítást a "$assemblyUrl" URL-címen található bájtos adatértékek használatával.</span><span class="sxs-lookup"><span data-stu-id="77a60-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="77a60-123">Ez a javasolt módszer nagy méretű összeállítások készítéséhez.</span><span class="sxs-lookup"><span data-stu-id="77a60-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="77a60-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77a60-124">PARAMETERS</span></span>

### <span data-ttu-id="77a60-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="77a60-125">-AssemblyData</span></span>
<span data-ttu-id="77a60-126">Az integrációs fiók összeszerelési bájtjának adatait.</span><span class="sxs-lookup"><span data-stu-id="77a60-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="77a60-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="77a60-127">-AssemblyFilePath</span></span>
<span data-ttu-id="77a60-128">Az integrációs fiók kódösszeállítás-fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="77a60-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="77a60-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="77a60-129">-ContentLink</span></span>
<span data-ttu-id="77a60-130">Nyilvánosan elérhető hivatkozás az integrációs fiókok összeállítási adatszolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="77a60-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="77a60-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a60-131">-DefaultProfile</span></span>
<span data-ttu-id="77a60-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77a60-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77a60-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77a60-133">-InputObject</span></span>
<span data-ttu-id="77a60-134">Egy integrációs fiók kódösszeállítása.</span><span class="sxs-lookup"><span data-stu-id="77a60-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="77a60-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="77a60-135">-Metadata</span></span>
<span data-ttu-id="77a60-136">Az integrációs fiók kódösszeállításának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="77a60-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="77a60-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77a60-137">-Name</span></span>
<span data-ttu-id="77a60-138">Az integrációs fiók kódösszeállításának neve.</span><span class="sxs-lookup"><span data-stu-id="77a60-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="77a60-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="77a60-139">-ParentName</span></span>
<span data-ttu-id="77a60-140">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="77a60-140">The integration account name.</span></span>

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

### <span data-ttu-id="77a60-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77a60-141">-ResourceGroupName</span></span>
<span data-ttu-id="77a60-142">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="77a60-142">The resource group name.</span></span>

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

### <span data-ttu-id="77a60-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77a60-143">-ResourceId</span></span>
<span data-ttu-id="77a60-144">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77a60-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="77a60-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77a60-145">-Confirm</span></span>
<span data-ttu-id="77a60-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77a60-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77a60-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77a60-147">-WhatIf</span></span>
<span data-ttu-id="77a60-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77a60-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77a60-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77a60-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77a60-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a60-150">CommonParameters</span></span>
<span data-ttu-id="77a60-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77a60-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a60-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77a60-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a60-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77a60-153">INPUTS</span></span>

### <span data-ttu-id="77a60-154">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="77a60-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="77a60-155">System. String</span><span class="sxs-lookup"><span data-stu-id="77a60-155">System.String</span></span>

## <span data-ttu-id="77a60-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77a60-156">OUTPUTS</span></span>

### <span data-ttu-id="77a60-157">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="77a60-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="77a60-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77a60-158">NOTES</span></span>

## <span data-ttu-id="77a60-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77a60-159">RELATED LINKS</span></span>
