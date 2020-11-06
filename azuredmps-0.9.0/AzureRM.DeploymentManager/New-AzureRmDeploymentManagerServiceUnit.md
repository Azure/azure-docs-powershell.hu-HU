---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490855"
---
# <span data-ttu-id="99228-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="99228-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="99228-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99228-102">SYNOPSIS</span></span>
<span data-ttu-id="99228-103">Új szolgáltatási egységet hoz létre a szolgáltatás topológiájában.</span><span class="sxs-lookup"><span data-stu-id="99228-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="99228-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99228-104">SYNTAX</span></span>

### <span data-ttu-id="99228-105">ByTopologyAndServiceNames (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99228-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99228-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="99228-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99228-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="99228-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99228-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="99228-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99228-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="99228-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99228-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="99228-110">DESCRIPTION</span></span>
<span data-ttu-id="99228-111">A **New-AzureRmDeploymentManagerServiceUnit** parancsmag szolgáltatásbeli topológiában hoz létre szolgáltatást, és egy olyan objektumot ad eredményül, amely a szolgáltatás egységét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="99228-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="99228-112">Adja meg a szolgáltatási egységet a nevével, a szolgáltatás nevével, a szolgáltatás topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="99228-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="99228-113">A parancsmag egy ServiceUnit objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="99228-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="99228-114">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="99228-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="99228-115">Példák</span><span class="sxs-lookup"><span data-stu-id="99228-115">EXAMPLES</span></span>

### <span data-ttu-id="99228-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99228-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="99228-117">Ez a parancsmag létrehoz egy új szolgáltatási egységet, amelynek neve ContosoService2Storage a ContosoResourceGroup-ban a ContosoService2-ban a ContosoServiceTopology-ben, a-ban található.</span><span class="sxs-lookup"><span data-stu-id="99228-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="99228-118">A Template és a Parameters fájlok relatív elérési utakként jelennek meg a szolgáltatás topológiájának ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="99228-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="99228-119">Az ebben a sablonban definiált erőforrásokat a program a cél erőforráscsoport service2ResourceGroup kell telepítenie, és a beállítás értéke növekvő értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="99228-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="99228-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="99228-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="99228-121">Ez a parancsmag létrehoz egy új szolgáltatási egységet, amelynek neve ContosoService2Storage a ContosoResourceGroup-ban a ContosoService2-ban a ContosoServiceTopology-ben, a-ban található.</span><span class="sxs-lookup"><span data-stu-id="99228-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="99228-122">A sablon és a paraméterek hivatkozását úgy kapja meg, hogy a rendszer a biztonsági topológia ContosoServiceTopology1 nem adta meg a biztonsági társítások ResourceId.</span><span class="sxs-lookup"><span data-stu-id="99228-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="99228-123">Az ebben a sablonban definiált erőforrásokat a program a cél erőforráscsoport service2ResourceGroup kell telepítenie, és meg kell felelnie a telepítés módjának.</span><span class="sxs-lookup"><span data-stu-id="99228-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="99228-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99228-124">PARAMETERS</span></span>

### <span data-ttu-id="99228-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99228-125">-AsJob</span></span>
<span data-ttu-id="99228-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99228-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99228-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99228-127">-DefaultProfile</span></span>
<span data-ttu-id="99228-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99228-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99228-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="99228-129">-DeploymentMode</span></span>
<span data-ttu-id="99228-130">A szolgáltatási egység erőforrásainak központi üzembe helyezéséhez használható üzembe helyezési mód.</span><span class="sxs-lookup"><span data-stu-id="99228-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="99228-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="99228-131">-Location</span></span>
<span data-ttu-id="99228-132">A szolgáltatási egység erőforrásának helye.</span><span class="sxs-lookup"><span data-stu-id="99228-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="99228-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99228-133">-Name</span></span>
<span data-ttu-id="99228-134">A szolgáltatás egységének neve.</span><span class="sxs-lookup"><span data-stu-id="99228-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="99228-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="99228-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="99228-136">A szolgáltatási egység erőforrásainak központi üzembe helyezéséhez használható üzembe helyezési mód.</span><span class="sxs-lookup"><span data-stu-id="99228-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="99228-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="99228-137">-ParametersUri</span></span>
<span data-ttu-id="99228-138">A szolgáltatási egység erőforrásainak központi üzembe helyezéséhez használható üzembe helyezési mód.</span><span class="sxs-lookup"><span data-stu-id="99228-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="99228-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99228-139">-ResourceGroupName</span></span>
<span data-ttu-id="99228-140">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="99228-140">The resource group.</span></span>

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

### <span data-ttu-id="99228-141">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="99228-141">-Service</span></span>
<span data-ttu-id="99228-142">Az a szolgáltatási objektum, amelyben a szolgáltatási egységet létre kívánja venni.</span><span class="sxs-lookup"><span data-stu-id="99228-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99228-143">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="99228-143">-ServiceName</span></span>
<span data-ttu-id="99228-144">Annak a szolgáltatásnak a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="99228-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="99228-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="99228-145">-ServiceResourceId</span></span>
<span data-ttu-id="99228-146">Annak a szolgáltatásnak az erőforrás-azonosítóját, amelyben létre kell hozva a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="99228-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99228-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="99228-147">-ServiceTopology</span></span>
<span data-ttu-id="99228-148">Annak a szolgáltatásnak a topológiai objektuma, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="99228-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99228-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="99228-149">-ServiceTopologyName</span></span>
<span data-ttu-id="99228-150">A szolgáltatás teljesítményszámláló topológiájának neve: Ez a szolgáltatás az egység része.</span><span class="sxs-lookup"><span data-stu-id="99228-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="99228-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="99228-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="99228-152">Annak a szolgáltatásnak a topológia-erőforrás-azonosítója, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="99228-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99228-153">-Címke</span><span class="sxs-lookup"><span data-stu-id="99228-153">-Tag</span></span>
<span data-ttu-id="99228-154">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="99228-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="99228-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99228-155">-TargetResourceGroup</span></span>
<span data-ttu-id="99228-156">Meghatározza azt a helyet, ahol a szolgáltatási egység alatti erőforrásokat üzembe helyezte.</span><span class="sxs-lookup"><span data-stu-id="99228-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="99228-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="99228-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="99228-158">A szolgáltatási egység erőforrásainak központi üzembe helyezéséhez használható üzembe helyezési mód.</span><span class="sxs-lookup"><span data-stu-id="99228-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="99228-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="99228-159">-TemplateUri</span></span>
<span data-ttu-id="99228-160">A szolgáltatási egység erőforrásainak központi üzembe helyezéséhez használható üzembe helyezési mód.</span><span class="sxs-lookup"><span data-stu-id="99228-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="99228-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99228-161">-Confirm</span></span>
<span data-ttu-id="99228-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99228-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99228-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99228-163">-WhatIf</span></span>
<span data-ttu-id="99228-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99228-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99228-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99228-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99228-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99228-166">CommonParameters</span></span>
<span data-ttu-id="99228-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99228-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99228-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99228-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99228-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99228-169">INPUTS</span></span>

### <span data-ttu-id="99228-170">Nincs</span><span class="sxs-lookup"><span data-stu-id="99228-170">None</span></span>

## <span data-ttu-id="99228-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99228-171">OUTPUTS</span></span>

### <span data-ttu-id="99228-172">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="99228-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="99228-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99228-173">NOTES</span></span>

## <span data-ttu-id="99228-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99228-174">RELATED LINKS</span></span>

[<span data-ttu-id="99228-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="99228-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="99228-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="99228-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="99228-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="99228-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)