---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387392"
---
# <span data-ttu-id="e663b-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e663b-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="e663b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e663b-102">SYNOPSIS</span></span>
<span data-ttu-id="e663b-103">Szolgáltatás topológiát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e663b-103">Creates a service topology.</span></span>

## <span data-ttu-id="e663b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e663b-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e663b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e663b-105">DESCRIPTION</span></span>
<span data-ttu-id="e663b-106">A **New-AzDeploymentManagerServiceTopology** parancsmag szolgáltatási topológiát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e663b-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="e663b-107">A visszaadott ServiceTopology objektumot helyben módosíthatja, majd módosíthatja a topológiát a Set-AzDeploymentManagerServiceTopology parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e663b-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="e663b-108">A visszaadott objektum</span><span class="sxs-lookup"><span data-stu-id="e663b-108">The returned object</span></span> 

<span data-ttu-id="e663b-109">A visszaadott objektumnak van egy ResourceId mezője, amely egy bevezetési erőforrásban hivatkozhat arra, hogy az ebben a szolgáltatás-topológiában deklarált szolgáltatások telepítve lesznek a bevezetésben.</span><span class="sxs-lookup"><span data-stu-id="e663b-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="e663b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e663b-110">EXAMPLES</span></span>

### <span data-ttu-id="e663b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e663b-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="e663b-112">Ez a parancsmag új szolgáltatás-topológiát hoz létre a ContosoResourceGroup erőforráscsoportban ContosoServiceTopology néven és közép-amerikai helyen.</span><span class="sxs-lookup"><span data-stu-id="e663b-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="e663b-113">A resource source ResourceId azt jelzi, hogy a szolgáltatásegység-definíciókhoz szükséges összetevőknek ebben a topológiában el kell olvasniuk a megadott összetevőforrásból.</span><span class="sxs-lookup"><span data-stu-id="e663b-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="e663b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e663b-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="e663b-115">Ez a parancsmag új szolgáltatás-topológiát hoz létre a ContosoResourceGroup erőforráscsoportban ContosoServiceTopology néven és közép-amerikai helyen.</span><span class="sxs-lookup"><span data-stu-id="e663b-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="e663b-116">Az összetevő-forráshivatkozások hiánya azt jelzi, hogy az ebben a topológiában a szolgáltatásegység-definíciókhoz szükséges összetevők abszolút SAS URI-kként biztosítanak a szolgáltatási egységben.</span><span class="sxs-lookup"><span data-stu-id="e663b-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="e663b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e663b-117">PARAMETERS</span></span>

### <span data-ttu-id="e663b-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="e663b-118">-ArtifactSourceId</span></span>
<span data-ttu-id="e663b-119">Annak az objektumforrásnak az azonosítója, amely a topológiát ékelteti.</span><span class="sxs-lookup"><span data-stu-id="e663b-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="e663b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e663b-120">-DefaultProfile</span></span>
<span data-ttu-id="e663b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e663b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e663b-122">-Location</span><span class="sxs-lookup"><span data-stu-id="e663b-122">-Location</span></span>
<span data-ttu-id="e663b-123">A topológia helye.</span><span class="sxs-lookup"><span data-stu-id="e663b-123">The location of the topology.</span></span>

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

### <span data-ttu-id="e663b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e663b-124">-Name</span></span>
<span data-ttu-id="e663b-125">A topológia neve.</span><span class="sxs-lookup"><span data-stu-id="e663b-125">The name of the topology.</span></span>

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

### <span data-ttu-id="e663b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e663b-126">-ResourceGroupName</span></span>
<span data-ttu-id="e663b-127">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="e663b-127">The resource group.</span></span>

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

### <span data-ttu-id="e663b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="e663b-128">-Tag</span></span>
<span data-ttu-id="e663b-129">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="e663b-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e663b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e663b-130">-Confirm</span></span>
<span data-ttu-id="e663b-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e663b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e663b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e663b-132">-WhatIf</span></span>
<span data-ttu-id="e663b-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e663b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e663b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e663b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e663b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e663b-135">CommonParameters</span></span>
<span data-ttu-id="e663b-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e663b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e663b-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e663b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e663b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e663b-138">INPUTS</span></span>

### <span data-ttu-id="e663b-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e663b-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e663b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e663b-140">OUTPUTS</span></span>

### <span data-ttu-id="e663b-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="e663b-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="e663b-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e663b-142">NOTES</span></span>

## <span data-ttu-id="e663b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e663b-143">RELATED LINKS</span></span>
