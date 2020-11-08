---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194684"
---
# <span data-ttu-id="eb810-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eb810-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="eb810-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb810-102">SYNOPSIS</span></span>
<span data-ttu-id="eb810-103">Létrehozza az integrációs fiók kódösszeállítását.</span><span class="sxs-lookup"><span data-stu-id="eb810-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="eb810-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb810-104">SYNTAX</span></span>

### <span data-ttu-id="eb810-105">ByIntegrationAccountAndFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb810-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb810-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="eb810-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb810-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="eb810-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb810-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="eb810-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb810-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="eb810-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb810-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="eb810-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb810-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="eb810-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb810-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="eb810-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb810-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="eb810-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb810-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb810-114">DESCRIPTION</span></span>
<span data-ttu-id="eb810-115">A **Get-AzIntegrationAccountAssembly** parancsmag új kódösszeállítást hoz létre az integrációs fiókban.</span><span class="sxs-lookup"><span data-stu-id="eb810-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="eb810-116">Példák</span><span class="sxs-lookup"><span data-stu-id="eb810-116">EXAMPLES</span></span>

### <span data-ttu-id="eb810-117">1. példa: új kódösszeállítás létrehozása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="eb810-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="eb810-118">Új kódösszeállítást hoz létre a "$localAssemblyFilePath" fájl elérési útján található fájl elérési útján található helyi fájl segítségével.</span><span class="sxs-lookup"><span data-stu-id="eb810-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="eb810-119">2. példa: új kódösszeállítás létrehozása bájtos adatszolgáltatással</span><span class="sxs-lookup"><span data-stu-id="eb810-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="eb810-120">Új kódösszeállítást hoz létre a "$assemblyContent" cellában lévő a bájt tömb használatával.</span><span class="sxs-lookup"><span data-stu-id="eb810-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="eb810-121">3. példa: új kódösszeállítás létrehozása tartalmi hivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="eb810-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="eb810-122">Új kódösszeállítást hoz létre a "$assemblyUrl" URL-címen található adatbájt-adat használatával.</span><span class="sxs-lookup"><span data-stu-id="eb810-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="eb810-123">Ez a javasolt módszer nagy méretű összeállítások készítéséhez.</span><span class="sxs-lookup"><span data-stu-id="eb810-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="eb810-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb810-124">PARAMETERS</span></span>

### <span data-ttu-id="eb810-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="eb810-125">-AssemblyData</span></span>
<span data-ttu-id="eb810-126">Az integrációs fiók összeszerelési bájtjának adatait.</span><span class="sxs-lookup"><span data-stu-id="eb810-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="eb810-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="eb810-127">-AssemblyFilePath</span></span>
<span data-ttu-id="eb810-128">Az integrációs fiók kódösszeállítás-fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="eb810-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="eb810-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="eb810-129">-ContentLink</span></span>
<span data-ttu-id="eb810-130">Nyilvánosan elérhető hivatkozás az integrációs fiókok összeállítási adatszolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="eb810-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="eb810-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb810-131">-DefaultProfile</span></span>
<span data-ttu-id="eb810-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb810-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb810-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="eb810-133">-Metadata</span></span>
<span data-ttu-id="eb810-134">Az integrációs fiók kódösszeállításának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="eb810-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="eb810-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb810-135">-Name</span></span>
<span data-ttu-id="eb810-136">Az integrációs fiók kódösszeállításának neve.</span><span class="sxs-lookup"><span data-stu-id="eb810-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="eb810-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="eb810-137">-ParentName</span></span>
<span data-ttu-id="eb810-138">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="eb810-138">The integration account name.</span></span>

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

### <span data-ttu-id="eb810-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eb810-139">-ParentObject</span></span>
<span data-ttu-id="eb810-140">Az integrációs fiók objektuma.</span><span class="sxs-lookup"><span data-stu-id="eb810-140">An integration account object.</span></span>

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

### <span data-ttu-id="eb810-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="eb810-141">-ParentResourceId</span></span>
<span data-ttu-id="eb810-142">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb810-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="eb810-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb810-143">-ResourceGroupName</span></span>
<span data-ttu-id="eb810-144">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="eb810-144">The resource group name.</span></span>

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

### <span data-ttu-id="eb810-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb810-145">-Confirm</span></span>
<span data-ttu-id="eb810-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb810-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb810-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb810-147">-WhatIf</span></span>
<span data-ttu-id="eb810-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb810-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb810-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb810-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb810-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb810-150">CommonParameters</span></span>
<span data-ttu-id="eb810-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb810-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb810-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb810-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb810-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb810-153">INPUTS</span></span>

### <span data-ttu-id="eb810-154">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="eb810-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="eb810-155">System. String</span><span class="sxs-lookup"><span data-stu-id="eb810-155">System.String</span></span>

## <span data-ttu-id="eb810-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb810-156">OUTPUTS</span></span>

### <span data-ttu-id="eb810-157">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eb810-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="eb810-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb810-158">NOTES</span></span>

## <span data-ttu-id="eb810-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb810-159">RELATED LINKS</span></span>