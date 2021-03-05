---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 992cd2a381e9eda89b9388ec1ed37f74a76e9adf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005414"
---
# <span data-ttu-id="c5719-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c5719-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="c5719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5719-102">SYNOPSIS</span></span>
<span data-ttu-id="c5719-103">Szolgáltatás eltávolítása a fürtből.</span><span class="sxs-lookup"><span data-stu-id="c5719-103">Remove a service from the cluster.</span></span> <span data-ttu-id="c5719-104">Csak az ARM szolgáltatásokat támogatja.</span><span class="sxs-lookup"><span data-stu-id="c5719-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="c5719-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5719-105">SYNTAX</span></span>

### <span data-ttu-id="c5719-106">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5719-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5719-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5719-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5719-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c5719-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5719-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5719-109">DESCRIPTION</span></span>
<span data-ttu-id="c5719-110">Ez a parancsmag eltávolítja a fürtszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="c5719-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="c5719-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5719-111">EXAMPLES</span></span>

### <span data-ttu-id="c5719-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5719-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="c5719-113">Ez a példa eltávolítja a "testApp~testService1" szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="c5719-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="c5719-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5719-114">PARAMETERS</span></span>

### <span data-ttu-id="c5719-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c5719-115">-ApplicationName</span></span>
<span data-ttu-id="c5719-116">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="c5719-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5719-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c5719-117">-ClusterName</span></span>
<span data-ttu-id="c5719-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="c5719-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5719-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5719-119">-DefaultProfile</span></span>
<span data-ttu-id="c5719-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5719-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5719-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c5719-121">-Force</span></span>
<span data-ttu-id="c5719-122">Eltávolítás kérdés nélkül.</span><span class="sxs-lookup"><span data-stu-id="c5719-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="c5719-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5719-123">-InputObject</span></span>
<span data-ttu-id="c5719-124">A szolgáltatáserőforrás.</span><span class="sxs-lookup"><span data-stu-id="c5719-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5719-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c5719-125">-Name</span></span>
<span data-ttu-id="c5719-126">Adja meg a szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="c5719-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5719-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5719-127">-PassThru</span></span>
<span data-ttu-id="c5719-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c5719-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c5719-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5719-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5719-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c5719-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5719-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5719-131">-ResourceId</span></span>
<span data-ttu-id="c5719-132">A szolgáltatás Erőforrásazonosítója arm.</span><span class="sxs-lookup"><span data-stu-id="c5719-132">Arm ResourceId of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5719-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5719-133">-Confirm</span></span>
<span data-ttu-id="c5719-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5719-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5719-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5719-135">-WhatIf</span></span>
<span data-ttu-id="c5719-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5719-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5719-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5719-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5719-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5719-138">CommonParameters</span></span>
<span data-ttu-id="c5719-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5719-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5719-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5719-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5719-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5719-141">INPUTS</span></span>

### <span data-ttu-id="c5719-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c5719-142">System.String</span></span>

### <span data-ttu-id="c5719-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="c5719-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="c5719-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5719-144">OUTPUTS</span></span>

### <span data-ttu-id="c5719-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5719-145">System.Boolean</span></span>

## <span data-ttu-id="c5719-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5719-146">NOTES</span></span>

## <span data-ttu-id="c5719-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5719-147">RELATED LINKS</span></span>
