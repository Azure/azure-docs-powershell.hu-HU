---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: d7e3055c6443faa2c85d63e6cfdb611cb7d2eb41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491580"
---
# <span data-ttu-id="24d65-101">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="24d65-101">New-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="24d65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24d65-102">SYNOPSIS</span></span>
<span data-ttu-id="24d65-103">Új szolgáltatási topológiát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="24d65-103">Creates a new service topology.</span></span>

## <span data-ttu-id="24d65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24d65-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d65-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24d65-105">DESCRIPTION</span></span>
<span data-ttu-id="24d65-106">A **New-AzureRmDeploymentManagerServiceTopology** parancsmag létrehoz egy szolgáltatási topológiát.</span><span class="sxs-lookup"><span data-stu-id="24d65-106">The **New-AzureRmDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="24d65-107">A visszaadott ServiceTopology-objektumot helyileg módosíthatja, majd a Set-AzureRmDeploymentManagerServiceTopology parancsmag használatával is alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="24d65-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="24d65-108">A visszaadott objektum</span><span class="sxs-lookup"><span data-stu-id="24d65-108">The returned object</span></span> 

<span data-ttu-id="24d65-109">A visszaadott objektumnak van egy ResourceId mezője, amely hivatkozhat a bevezetési erőforrásokra, így jelezve, hogy az ebben a szolgáltatási topológiában bejelentett szolgáltatások üzembe helyezése a kivezetésben történik.</span><span class="sxs-lookup"><span data-stu-id="24d65-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="24d65-110">Példák</span><span class="sxs-lookup"><span data-stu-id="24d65-110">EXAMPLES</span></span>

### <span data-ttu-id="24d65-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24d65-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="24d65-112">Ez a parancsmag új szolgáltatási topológiát hoz létre a ContosoResourceGroup nevű erőforráscsoport-ContosoServiceTopology és a közép-amerikai helyen.</span><span class="sxs-lookup"><span data-stu-id="24d65-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="24d65-113">Az ereklyék forrása ResourceId azt jelzi, hogy az ebben a topológiában a szolgáltatási egység meghatározásához szükséges leleteknek a megadott tárgyi forrásból kell olvasni.</span><span class="sxs-lookup"><span data-stu-id="24d65-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="24d65-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="24d65-114">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="24d65-115">Ez a parancsmag új szolgáltatási topológiát hoz létre a ContosoResourceGroup nevű erőforráscsoport-ContosoServiceTopology és a közép-amerikai helyen.</span><span class="sxs-lookup"><span data-stu-id="24d65-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="24d65-116">A lelet-forrás hivatkozás hiánya azt jelzi, hogy az ebben a topológiában a szolgáltatási egység meghatározásához szükséges leletek a szolgáltatási egységben abszolút SAS URI-ként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="24d65-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="24d65-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24d65-117">PARAMETERS</span></span>

### <span data-ttu-id="24d65-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="24d65-118">-ArtifactSourceId</span></span>
<span data-ttu-id="24d65-119">Annak a tárgynak az azonosítója, ahol a topológiát alkotó leletek vannak tárolva.</span><span class="sxs-lookup"><span data-stu-id="24d65-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="24d65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d65-120">-DefaultProfile</span></span>
<span data-ttu-id="24d65-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24d65-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d65-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="24d65-122">-Location</span></span>
<span data-ttu-id="24d65-123">A topológia helye.</span><span class="sxs-lookup"><span data-stu-id="24d65-123">The location of the topology.</span></span>

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

### <span data-ttu-id="24d65-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24d65-124">-Name</span></span>
<span data-ttu-id="24d65-125">A topológia neve.</span><span class="sxs-lookup"><span data-stu-id="24d65-125">The name of the topology.</span></span>

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

### <span data-ttu-id="24d65-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d65-126">-ResourceGroupName</span></span>
<span data-ttu-id="24d65-127">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="24d65-127">The resource group.</span></span>

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

### <span data-ttu-id="24d65-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="24d65-128">-Tag</span></span>
<span data-ttu-id="24d65-129">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="24d65-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="24d65-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24d65-130">-Confirm</span></span>
<span data-ttu-id="24d65-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24d65-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d65-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d65-132">-WhatIf</span></span>
<span data-ttu-id="24d65-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24d65-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24d65-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24d65-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d65-135">CommonParameters</span></span>
<span data-ttu-id="24d65-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24d65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d65-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d65-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d65-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d65-138">INPUTS</span></span>

### <span data-ttu-id="24d65-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="24d65-139">None</span></span>

## <span data-ttu-id="24d65-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d65-140">OUTPUTS</span></span>

### <span data-ttu-id="24d65-141">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="24d65-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="24d65-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24d65-142">NOTES</span></span>

## <span data-ttu-id="24d65-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24d65-143">RELATED LINKS</span></span>

[<span data-ttu-id="24d65-144">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="24d65-144">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="24d65-145">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="24d65-145">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="24d65-146">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="24d65-146">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)