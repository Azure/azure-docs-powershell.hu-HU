---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208630"
---
# <span data-ttu-id="02233-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="02233-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="02233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02233-102">SYNOPSIS</span></span>
<span data-ttu-id="02233-103">Szolgáltatási egységet hoz létre a megadott szolgáltatás- és szolgáltatás topológia alapján.</span><span class="sxs-lookup"><span data-stu-id="02233-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="02233-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02233-104">SYNTAX</span></span>

### <span data-ttu-id="02233-105">ByTopologyAndServiceNames (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02233-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02233-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="02233-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02233-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="02233-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02233-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="02233-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02233-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="02233-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02233-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02233-110">DESCRIPTION</span></span>
<span data-ttu-id="02233-111">A **New-AzDeploymentManagerServiceUnit** parancsmag szolgáltatás topológia szolgáltatása alatt hoz létre egy szolgáltatást, és visszaad egy objektumot, amely az adott szolgáltatási egységet képviseli.</span><span class="sxs-lookup"><span data-stu-id="02233-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="02233-112">Adja meg a szolgáltatási egység nevét, szolgáltatásnevét, szolgáltatás topológiáját és az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="02233-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="02233-113">A parancsmag ServiceUnit-objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="02233-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="02233-114">Ezt az objektumot helyben módosíthatja, majd a Set-AzDeploymentManagerService alkalmazhatja a szolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="02233-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="02233-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02233-115">EXAMPLES</span></span>

### <span data-ttu-id="02233-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="02233-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="02233-117">Ez a parancsmag létrehoz egy új szolgáltatási egységet a ContosoService2Storage névvel a ContosoResourceGroup csoportban a ContosoService2 topológiában a ContosoServiceTopology szolgáltatásban, az Egyesült Államok középső területén.</span><span class="sxs-lookup"><span data-stu-id="02233-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="02233-118">A sablon- és paraméterfájlok relatív elérési utakként vannak definiálva a ContosoServiceTopology szolgáltatás topológia szolgáltatás topológiája által hivatkozott összetevő-forráshelyhez.</span><span class="sxs-lookup"><span data-stu-id="02233-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="02233-119">A sablonban definiált erőforrásokat a célerőforrás-csoport service2ResourceGroup szolgáltatásban kell üzembe helyezni úgy, hogy a telepítési mód Növekményes.</span><span class="sxs-lookup"><span data-stu-id="02233-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="02233-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="02233-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="02233-121">Ez a parancsmag létrehoz egy új szolgáltatási egységet a ContosoService2Storage névvel a ContosoResourceGroup csoportban a ContosoService2 topológiában a ContosoServiceTopology szolgáltatásban, az Egyesült Államok középső területén.</span><span class="sxs-lookup"><span data-stu-id="02233-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="02233-122">A sablon- és paraméterhivatkozások mint SAS Uri mint a ContosoServiceTopology1 szolgáltatás topológia szolgáltatás topológiája nem tartalmazta az ResourceId összetevő összetevőt.</span><span class="sxs-lookup"><span data-stu-id="02233-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="02233-123">A sablonban definiált erőforrásokat a célerőforrás-csoport service2ResourceGroup szolgáltatásban kell üzembe helyezni úgy, hogy a telepítési mód Befejeződött.</span><span class="sxs-lookup"><span data-stu-id="02233-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="02233-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02233-124">PARAMETERS</span></span>

### <span data-ttu-id="02233-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02233-125">-AsJob</span></span>
<span data-ttu-id="02233-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="02233-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02233-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02233-127">-DefaultProfile</span></span>
<span data-ttu-id="02233-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02233-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02233-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="02233-129">-DeploymentMode</span></span>
<span data-ttu-id="02233-130">Az erőforrások szolgáltatási egységben való telepítésekor használt telepítési mód.</span><span class="sxs-lookup"><span data-stu-id="02233-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-131">-Location</span><span class="sxs-lookup"><span data-stu-id="02233-131">-Location</span></span>
<span data-ttu-id="02233-132">A szolgáltatásegység-erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="02233-132">The location of the service unit resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-133">-Name</span><span class="sxs-lookup"><span data-stu-id="02233-133">-Name</span></span>
<span data-ttu-id="02233-134">A szolgáltatási egység neve.</span><span class="sxs-lookup"><span data-stu-id="02233-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="02233-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="02233-136">A paraméterfájl elérési útja az összetevő-forráshoz képest.</span><span class="sxs-lookup"><span data-stu-id="02233-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="02233-137">A ServiceTopology összetevőben hivatkozni kell az ArtifactSource összetevőre.</span><span class="sxs-lookup"><span data-stu-id="02233-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="02233-138">-ParametersUri</span></span>
<span data-ttu-id="02233-139">Az SAS Uri a paraméterfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="02233-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="02233-140">Ha az ArtifactSourceId függvényre a ServiceTopology függvényben hivatkozik, adja meg a relatív elérési utat a ParametersArtifactSourceRelativePath használatával.</span><span class="sxs-lookup"><span data-stu-id="02233-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02233-141">-ResourceGroupName</span></span>
<span data-ttu-id="02233-142">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="02233-142">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="02233-143">-ServiceName</span></span>
<span data-ttu-id="02233-144">Annak a szolgáltatásnak a neve, amely részét képezi a szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="02233-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="02233-145">-ServiceObject</span></span>
<span data-ttu-id="02233-146">Az a szolgáltatásobjektum, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="02233-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="02233-147">-ServiceResourceId</span></span>
<span data-ttu-id="02233-148">Az a szolgáltatáserőforrás-azonosító, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="02233-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="02233-149">-ServiceTopologyName</span></span>
<span data-ttu-id="02233-150">Annak a szolgáltatás-topológiának a neve, amely része ennek a szolgáltatásegységnek.</span><span class="sxs-lookup"><span data-stu-id="02233-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="02233-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="02233-152">Az a szolgáltatás topológia objektum, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="02233-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="02233-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="02233-154">Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hoznunk a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="02233-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="02233-155">-Tag</span></span>
<span data-ttu-id="02233-156">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="02233-156">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02233-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02233-157">-TargetResourceGroup</span></span>
<span data-ttu-id="02233-158">Azt a helyet határozza meg, ahol a szolgáltatási egység erőforrásait a rendszer üzembe helyezheti.</span><span class="sxs-lookup"><span data-stu-id="02233-158">Determines the location where resources under the service unit would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="02233-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="02233-160">A sablonfájl elérési útja az elemforráshoz képest.</span><span class="sxs-lookup"><span data-stu-id="02233-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="02233-161">A ServiceTopology összetevőben hivatkozni kell az ArtifactSource összetevőre.</span><span class="sxs-lookup"><span data-stu-id="02233-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="02233-162">-TemplateUri</span></span>
<span data-ttu-id="02233-163">Az SAS Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="02233-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="02233-164">Ha a ServiceTopology függvényben hivatkozott az ArtifactSourceId függvényre, adja meg a relatív elérési utat a TemplateArtifactSourceRelativePath használatával.</span><span class="sxs-lookup"><span data-stu-id="02233-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02233-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02233-165">-Confirm</span></span>
<span data-ttu-id="02233-166">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="02233-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02233-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02233-167">-WhatIf</span></span>
<span data-ttu-id="02233-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="02233-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02233-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02233-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02233-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02233-170">CommonParameters</span></span>
<span data-ttu-id="02233-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02233-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02233-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02233-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02233-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02233-173">INPUTS</span></span>

### <span data-ttu-id="02233-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="02233-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="02233-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02233-175">OUTPUTS</span></span>

### <span data-ttu-id="02233-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="02233-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="02233-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02233-177">NOTES</span></span>

## <span data-ttu-id="02233-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02233-178">RELATED LINKS</span></span>
