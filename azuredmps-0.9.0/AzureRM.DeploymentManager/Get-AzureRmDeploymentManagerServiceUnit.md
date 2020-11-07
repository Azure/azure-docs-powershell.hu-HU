---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671705"
---
# <span data-ttu-id="a2163-101">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a2163-101">Get-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="a2163-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2163-102">SYNOPSIS</span></span>
<span data-ttu-id="a2163-103">Kinyer egy szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="a2163-103">Gets a service unit.</span></span>

## <span data-ttu-id="a2163-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2163-104">SYNTAX</span></span>

### <span data-ttu-id="a2163-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2163-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2163-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="a2163-106">ByServiceObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2163-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a2163-107">ByServiceResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2163-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a2163-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2163-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a2163-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2163-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2163-110">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2163-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="a2163-111">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2163-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2163-112">DESCRIPTION</span></span>
<span data-ttu-id="a2163-113">A **Get-AzureRmDeploymentManagerServiceUnit** parancsmag egy szolgáltatási egységet kap a szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="a2163-113">The **Get-AzureRmDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="a2163-114">Adja meg a szolgáltatás mértékegységét az annak nevével, az azt tartalmazó szolgáltatással, a szolgáltatás topológiájának nevével és az erőforrás csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="a2163-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="a2163-115">Másik lehetőségként megadhatja a ServiceUnit objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a2163-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="a2163-116">Ezt az objektumot helyileg módosíthatja, majd a Set-AzureRmDeploymentManagerServiceUnit parancsmag használatával alkalmazhatja a megfelelő módosításokat.</span><span class="sxs-lookup"><span data-stu-id="a2163-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzureRmDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="a2163-117">Példák</span><span class="sxs-lookup"><span data-stu-id="a2163-117">EXAMPLES</span></span>

### <span data-ttu-id="a2163-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2163-118">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="a2163-119">Ez a parancs egy ContosoService1Storage nevű ContosoService1 kap a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="a2163-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a2163-120">2. példa: szolgáltatási egység beszerzése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="a2163-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="a2163-121">Ez a parancs egy ContosoService1Storage nevű ContosoService1 kap a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="a2163-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a2163-122">3. példa: szolgáltatás-egység beszerzése a Service Unit objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="a2163-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="a2163-123">Ez a parancs egy olyan szolgáltatási egységet kap, amelynek a neve, a szolgáltatás neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceUnitObject, a szolgáltatásnév, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="a2163-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="a2163-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2163-124">PARAMETERS</span></span>

### <span data-ttu-id="a2163-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2163-125">-DefaultProfile</span></span>
<span data-ttu-id="a2163-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2163-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2163-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2163-127">-Name</span></span>
<span data-ttu-id="a2163-128">A szolgáltatás egységének neve.</span><span class="sxs-lookup"><span data-stu-id="a2163-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2163-129">-ResourceGroupName</span></span>
<span data-ttu-id="a2163-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="a2163-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2163-131">-ResourceId</span></span>
<span data-ttu-id="a2163-132">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a2163-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-133">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="a2163-133">-Service</span></span>
<span data-ttu-id="a2163-134">Az a szolgáltatási objektum, amelyben a szolgáltatási egységet létre kívánja venni.</span><span class="sxs-lookup"><span data-stu-id="a2163-134">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-135">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a2163-135">-ServiceName</span></span>
<span data-ttu-id="a2163-136">Annak a szolgáltatásnak a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="a2163-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a2163-137">-ServiceResourceId</span></span>
<span data-ttu-id="a2163-138">Annak a szolgáltatásnak az erőforrás-azonosítóját, amelyben létre kell hozva a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="a2163-138">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-139">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="a2163-139">-ServiceTopology</span></span>
<span data-ttu-id="a2163-140">Annak a szolgáltatásnak a topológiai objektuma, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="a2163-140">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a2163-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="a2163-141">-ServiceTopologyName</span></span>
<span data-ttu-id="a2163-142">Annak a szolgáltatási topológiának a neve, amely a szolgáltatási egység része.</span><span class="sxs-lookup"><span data-stu-id="a2163-142">The name of the service topology the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a2163-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="a2163-144">Annak a szolgáltatásnak a topológia-erőforrás-azonosítója, amelyben létre kell tenni a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="a2163-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a2163-145">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a2163-145">-ServiceUnit</span></span>
<span data-ttu-id="a2163-146">A Service Unit Resource objektum.</span><span class="sxs-lookup"><span data-stu-id="a2163-146">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2163-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2163-147">CommonParameters</span></span>
<span data-ttu-id="a2163-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2163-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2163-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2163-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2163-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2163-150">INPUTS</span></span>

### <span data-ttu-id="a2163-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="a2163-151">None</span></span>

## <span data-ttu-id="a2163-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2163-152">OUTPUTS</span></span>

### <span data-ttu-id="a2163-153">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="a2163-153">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a2163-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2163-154">NOTES</span></span>

## <span data-ttu-id="a2163-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2163-155">RELATED LINKS</span></span>

[<span data-ttu-id="a2163-156">Új – AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a2163-156">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="a2163-157">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a2163-157">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="a2163-158">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a2163-158">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)