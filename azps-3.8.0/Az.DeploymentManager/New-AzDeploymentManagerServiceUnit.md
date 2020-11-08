---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014381"
---
# <span data-ttu-id="247ef-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="247ef-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="247ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="247ef-102">SYNOPSIS</span></span>
<span data-ttu-id="247ef-103">A megadott szolgáltatás és szolgáltatás topológiája alatt létrehoz egy szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="247ef-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="247ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="247ef-104">SYNTAX</span></span>

### <span data-ttu-id="247ef-105">ByTopologyAndServiceNames (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="247ef-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="247ef-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="247ef-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="247ef-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="247ef-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="247ef-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="247ef-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="247ef-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="247ef-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="247ef-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="247ef-110">DESCRIPTION</span></span>
<span data-ttu-id="247ef-111">A **New-AzDeploymentManagerServiceUnit** parancsmag szolgáltatásbeli topológiában hoz létre szolgáltatást, és egy olyan objektumot ad eredményül, amely a szolgáltatás egységét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="247ef-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="247ef-112">Adja meg a szolgáltatási egységet a nevével, a szolgáltatás nevével, a szolgáltatás topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="247ef-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="247ef-113">A parancsmag egy ServiceUnit objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="247ef-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="247ef-114">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="247ef-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="247ef-115">Példák</span><span class="sxs-lookup"><span data-stu-id="247ef-115">EXAMPLES</span></span>

### <span data-ttu-id="247ef-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="247ef-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="247ef-117">Ez a parancsmag létrehoz egy új szolgáltatási egységet, amelynek neve ContosoService2Storage a ContosoResourceGroup-ban a ContosoService2-ban a ContosoServiceTopology-ben, a-ban található.</span><span class="sxs-lookup"><span data-stu-id="247ef-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="247ef-118">A Template és a Parameters fájlok relatív elérési utakként jelennek meg a szolgáltatás topológiájának ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="247ef-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="247ef-119">Az ebben a sablonban definiált erőforrásokat a program a cél erőforráscsoport service2ResourceGroup kell telepítenie, és a beállítás értéke növekvő értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="247ef-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="247ef-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="247ef-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="247ef-121">Ez a parancsmag létrehoz egy új szolgáltatási egységet, amelynek neve ContosoService2Storage a ContosoResourceGroup-ban a ContosoService2-ban a ContosoServiceTopology-ben, a-ban található.</span><span class="sxs-lookup"><span data-stu-id="247ef-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="247ef-122">A sablon és a paraméterek hivatkozását úgy kapja meg, hogy a rendszer a biztonsági topológia ContosoServiceTopology1 nem adta meg a biztonsági társítások ResourceId.</span><span class="sxs-lookup"><span data-stu-id="247ef-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="247ef-123">Az ebben a sablonban definiált erőforrásokat a program a cél erőforráscsoport service2ResourceGroup kell telepítenie, és meg kell felelnie a telepítés módjának.</span><span class="sxs-lookup"><span data-stu-id="247ef-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="247ef-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="247ef-124">PARAMETERS</span></span>

### <span data-ttu-id="247ef-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="247ef-125">-AsJob</span></span>
<span data-ttu-id="247ef-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="247ef-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="247ef-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247ef-127">-DefaultProfile</span></span>
<span data-ttu-id="247ef-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="247ef-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="247ef-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="247ef-129">-DeploymentMode</span></span>
<span data-ttu-id="247ef-130">A szolgáltatási egység erőforrásainak központi üzembe helyezéséhez használható üzembe helyezési mód.</span><span class="sxs-lookup"><span data-stu-id="247ef-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="247ef-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="247ef-131">-Location</span></span>
<span data-ttu-id="247ef-132">A szolgáltatási egység erőforrásának helye.</span><span class="sxs-lookup"><span data-stu-id="247ef-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="247ef-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="247ef-133">-Name</span></span>
<span data-ttu-id="247ef-134">A szolgáltatás egységének neve.</span><span class="sxs-lookup"><span data-stu-id="247ef-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="247ef-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="247ef-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="247ef-136">A paraméterek fájl elérési útvonala a tárgy forrásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="247ef-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="247ef-137">A ServiceTopology-ban hivatkozni kell a ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="247ef-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="247ef-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="247ef-138">-ParametersUri</span></span>
<span data-ttu-id="247ef-139">A SAS URI a parameters (paraméterek) fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="247ef-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="247ef-140">Ha a ArtifactSourceId hivatkoztak a ServiceTopology, adja meg a relatív elérési utat a ParametersArtifactSourceRelativePath használatával.</span><span class="sxs-lookup"><span data-stu-id="247ef-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="247ef-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="247ef-141">-ResourceGroupName</span></span>
<span data-ttu-id="247ef-142">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="247ef-142">The resource group.</span></span>

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

### <span data-ttu-id="247ef-143">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="247ef-143">-ServiceName</span></span>
<span data-ttu-id="247ef-144">Annak a szolgáltatásnak a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="247ef-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="247ef-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="247ef-145">-ServiceObject</span></span>
<span data-ttu-id="247ef-146">Az a szolgáltatási objektum, amelyben a szolgáltatási egységet létre kívánja venni.</span><span class="sxs-lookup"><span data-stu-id="247ef-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="247ef-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="247ef-147">-ServiceResourceId</span></span>
<span data-ttu-id="247ef-148">Annak a szolgáltatásnak az erőforrás-azonosítóját, amelyben létre kell hozva a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="247ef-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="247ef-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="247ef-149">-ServiceTopologyName</span></span>
<span data-ttu-id="247ef-150">Annak a szolgáltatási topológiának a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="247ef-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="247ef-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="247ef-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="247ef-152">Annak a szolgáltatásnak a topológiai objektuma, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="247ef-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="247ef-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="247ef-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="247ef-154">Annak a szolgáltatásnak a topológia-erőforrás-azonosítója, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="247ef-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="247ef-155">-Címke</span><span class="sxs-lookup"><span data-stu-id="247ef-155">-Tag</span></span>
<span data-ttu-id="247ef-156">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="247ef-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="247ef-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="247ef-157">-TargetResourceGroup</span></span>
<span data-ttu-id="247ef-158">Meghatározza azt a helyet, ahol a szolgáltatási egység alatti erőforrásokat üzembe helyezte.</span><span class="sxs-lookup"><span data-stu-id="247ef-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="247ef-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="247ef-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="247ef-160">A sablonfájl elérési útvonala a tárgy forrásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="247ef-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="247ef-161">A ServiceTopology-ban hivatkozni kell a ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="247ef-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="247ef-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="247ef-162">-TemplateUri</span></span>
<span data-ttu-id="247ef-163">A SAS-URI a sablonfájl.</span><span class="sxs-lookup"><span data-stu-id="247ef-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="247ef-164">Ha a ArtifactSourceId hivatkoztak a ServiceTopology, adja meg a relatív elérési utat a TemplateArtifactSourceRelativePath használatával.</span><span class="sxs-lookup"><span data-stu-id="247ef-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="247ef-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="247ef-165">-Confirm</span></span>
<span data-ttu-id="247ef-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="247ef-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247ef-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247ef-167">-WhatIf</span></span>
<span data-ttu-id="247ef-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="247ef-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247ef-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="247ef-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247ef-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247ef-170">CommonParameters</span></span>
<span data-ttu-id="247ef-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="247ef-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247ef-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="247ef-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247ef-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="247ef-173">INPUTS</span></span>

### <span data-ttu-id="247ef-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="247ef-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="247ef-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="247ef-175">OUTPUTS</span></span>

### <span data-ttu-id="247ef-176">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="247ef-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="247ef-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="247ef-177">NOTES</span></span>

## <span data-ttu-id="247ef-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="247ef-178">RELATED LINKS</span></span>
