---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017805"
---
# <span data-ttu-id="c3fe3-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="c3fe3-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="c3fe3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fe3-103">A megadott szolgáltatás és szolgáltatás topológiája alatt létrehoz egy szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="c3fe3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3fe3-104">SYNTAX</span></span>

### <span data-ttu-id="c3fe3-105">ByTopologyAndServiceNames (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3fe3-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3fe3-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c3fe3-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fe3-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c3fe3-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fe3-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="c3fe3-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fe3-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c3fe3-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3fe3-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3fe3-110">DESCRIPTION</span></span>
<span data-ttu-id="c3fe3-111">A **New-AzDeploymentManagerServiceUnit** parancsmag szolgáltatásbeli topológiában hoz létre szolgáltatást, és egy olyan objektumot ad eredményül, amely a szolgáltatás egységét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="c3fe3-112">Adja meg a szolgáltatási egységet a nevével, a szolgáltatás nevével, a szolgáltatás topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="c3fe3-113">A parancsmag egy ServiceUnit objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="c3fe3-114">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="c3fe3-115">Példák</span><span class="sxs-lookup"><span data-stu-id="c3fe3-115">EXAMPLES</span></span>

### <span data-ttu-id="c3fe3-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3fe3-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="c3fe3-117">Ez a parancsmag létrehoz egy új szolgáltatási egységet, amelynek neve ContosoService2Storage a ContosoResourceGroup-ban a ContosoService2-ban a ContosoServiceTopology-ben, a-ban található.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="c3fe3-118">A Template és a Parameters fájlok relatív elérési utakként jelennek meg a szolgáltatás topológiájának ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="c3fe3-119">Az ebben a sablonban definiált erőforrásokat a program a cél erőforráscsoport service2ResourceGroup kell telepítenie, és a beállítás értéke növekvő értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="c3fe3-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3fe3-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="c3fe3-121">Ez a parancsmag létrehoz egy új szolgáltatási egységet, amelynek neve ContosoService2Storage a ContosoResourceGroup-ban a ContosoService2-ban a ContosoServiceTopology-ben, a-ban található.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="c3fe3-122">A sablon és a paraméterek hivatkozását úgy kapja meg, hogy a rendszer a biztonsági topológia ContosoServiceTopology1 nem adta meg a biztonsági társítások ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="c3fe3-123">Az ebben a sablonban definiált erőforrásokat a program a cél erőforráscsoport service2ResourceGroup kell telepítenie, és meg kell felelnie a telepítés módjának.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="c3fe3-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3fe3-124">PARAMETERS</span></span>

### <span data-ttu-id="c3fe3-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3fe3-125">-AsJob</span></span>
<span data-ttu-id="c3fe3-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c3fe3-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3fe3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fe3-127">-DefaultProfile</span></span>
<span data-ttu-id="c3fe3-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3fe3-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="c3fe3-129">-DeploymentMode</span></span>
<span data-ttu-id="c3fe3-130">A szolgáltatási egység erőforrásainak központi üzembe helyezéséhez használható üzembe helyezési mód.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="c3fe3-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="c3fe3-131">-Location</span></span>
<span data-ttu-id="c3fe3-132">A szolgáltatási egység erőforrásának helye.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="c3fe3-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3fe3-133">-Name</span></span>
<span data-ttu-id="c3fe3-134">A szolgáltatás egységének neve.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="c3fe3-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c3fe3-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="c3fe3-136">A paraméterek fájl elérési útvonala a tárgy forrásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="c3fe3-137">A ServiceTopology-ban hivatkozni kell a ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="c3fe3-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="c3fe3-138">-ParametersUri</span></span>
<span data-ttu-id="c3fe3-139">A SAS URI a parameters (paraméterek) fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="c3fe3-140">Ha a ArtifactSourceId hivatkoztak a ServiceTopology, adja meg a relatív elérési utat a ParametersArtifactSourceRelativePath használatával.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="c3fe3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fe3-141">-ResourceGroupName</span></span>
<span data-ttu-id="c3fe3-142">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-142">The resource group.</span></span>

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

### <span data-ttu-id="c3fe3-143">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="c3fe3-143">-ServiceName</span></span>
<span data-ttu-id="c3fe3-144">Annak a szolgáltatásnak a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="c3fe3-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="c3fe3-145">-ServiceObject</span></span>
<span data-ttu-id="c3fe3-146">Az a szolgáltatási objektum, amelyben a szolgáltatási egységet létre kívánja venni.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c3fe3-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c3fe3-147">-ServiceResourceId</span></span>
<span data-ttu-id="c3fe3-148">Annak a szolgáltatásnak az erőforrás-azonosítóját, amelyben létre kell hozva a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c3fe3-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="c3fe3-149">-ServiceTopologyName</span></span>
<span data-ttu-id="c3fe3-150">Annak a szolgáltatási topológiának a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="c3fe3-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c3fe3-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="c3fe3-152">Annak a szolgáltatásnak a topológiai objektuma, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c3fe3-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c3fe3-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="c3fe3-154">Annak a szolgáltatásnak a topológia-erőforrás-azonosítója, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c3fe3-155">-Címke</span><span class="sxs-lookup"><span data-stu-id="c3fe3-155">-Tag</span></span>
<span data-ttu-id="c3fe3-156">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="c3fe3-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c3fe3-157">-TargetResourceGroup</span></span>
<span data-ttu-id="c3fe3-158">Meghatározza azt a helyet, ahol a szolgáltatási egység alatti erőforrásokat üzembe helyezte.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="c3fe3-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c3fe3-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="c3fe3-160">A sablonfájl elérési útvonala a tárgy forrásához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="c3fe3-161">A ServiceTopology-ban hivatkozni kell a ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="c3fe3-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c3fe3-162">-TemplateUri</span></span>
<span data-ttu-id="c3fe3-163">A SAS-URI a sablonfájl.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="c3fe3-164">Ha a ArtifactSourceId hivatkoztak a ServiceTopology, adja meg a relatív elérési utat a TemplateArtifactSourceRelativePath használatával.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="c3fe3-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3fe3-165">-Confirm</span></span>
<span data-ttu-id="c3fe3-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3fe3-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3fe3-167">-WhatIf</span></span>
<span data-ttu-id="c3fe3-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3fe3-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3fe3-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fe3-170">CommonParameters</span></span>
<span data-ttu-id="c3fe3-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3fe3-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fe3-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3fe3-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fe3-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3fe3-173">INPUTS</span></span>

### <span data-ttu-id="c3fe3-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c3fe3-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c3fe3-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3fe3-175">OUTPUTS</span></span>

### <span data-ttu-id="c3fe3-176">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c3fe3-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c3fe3-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3fe3-177">NOTES</span></span>

## <span data-ttu-id="c3fe3-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3fe3-178">RELATED LINKS</span></span>
