---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1475296638cec105713eaa390bcce6552e5502ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024434"
---
# <span data-ttu-id="6f780-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6f780-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="6f780-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f780-102">SYNOPSIS</span></span>
<span data-ttu-id="6f780-103">Szolgáltatás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="6f780-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="6f780-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f780-104">SYNTAX</span></span>

### <span data-ttu-id="6f780-105">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f780-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f780-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f780-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f780-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f780-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f780-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f780-108">DESCRIPTION</span></span>
<span data-ttu-id="6f780-109">Ez a parancsmag eltávolítja a fürtöt egy szolgáltatási űrlapon.</span><span class="sxs-lookup"><span data-stu-id="6f780-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="6f780-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6f780-110">EXAMPLES</span></span>

### <span data-ttu-id="6f780-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6f780-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="6f780-112">Ebben a példában a "testApp ~ testService1" szolgáltatást fogja törölni.</span><span class="sxs-lookup"><span data-stu-id="6f780-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="6f780-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f780-113">PARAMETERS</span></span>

### <span data-ttu-id="6f780-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6f780-114">-ApplicationName</span></span>
<span data-ttu-id="6f780-115">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="6f780-115">Specify the name of the application.</span></span>

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

### <span data-ttu-id="6f780-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="6f780-116">-ClusterName</span></span>
<span data-ttu-id="6f780-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="6f780-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6f780-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f780-118">-DefaultProfile</span></span>
<span data-ttu-id="6f780-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f780-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f780-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6f780-120">-Force</span></span>
<span data-ttu-id="6f780-121">Eltávolítás kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="6f780-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="6f780-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f780-122">-InputObject</span></span>
<span data-ttu-id="6f780-123">A szolgáltatás erőforrása.</span><span class="sxs-lookup"><span data-stu-id="6f780-123">The service resource.</span></span>

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

### <span data-ttu-id="6f780-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f780-124">-Name</span></span>
<span data-ttu-id="6f780-125">Adja meg a szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="6f780-125">Specify the name of the service.</span></span>

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

### <span data-ttu-id="6f780-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f780-126">-PassThru</span></span>
<span data-ttu-id="6f780-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6f780-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6f780-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f780-128">-ResourceGroupName</span></span>
<span data-ttu-id="6f780-129">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="6f780-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6f780-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f780-130">-ResourceId</span></span>
<span data-ttu-id="6f780-131">A szolgáltatás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6f780-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="6f780-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6f780-132">-Confirm</span></span>
<span data-ttu-id="6f780-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f780-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f780-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f780-134">-WhatIf</span></span>
<span data-ttu-id="6f780-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6f780-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f780-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6f780-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f780-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f780-137">CommonParameters</span></span>
<span data-ttu-id="6f780-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f780-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f780-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f780-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f780-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f780-140">INPUTS</span></span>

### <span data-ttu-id="6f780-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6f780-141">System.String</span></span>

### <span data-ttu-id="6f780-142">Microsoft. Azure. Command. ServiceFabric. models. PSService</span><span class="sxs-lookup"><span data-stu-id="6f780-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="6f780-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f780-143">OUTPUTS</span></span>

### <span data-ttu-id="6f780-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f780-144">System.Boolean</span></span>

## <span data-ttu-id="6f780-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f780-145">NOTES</span></span>

## <span data-ttu-id="6f780-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f780-146">RELATED LINKS</span></span>
