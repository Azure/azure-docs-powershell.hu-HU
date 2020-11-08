---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 8dc06a9ce860dfb6e01c79674dd414eedb51df17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188169"
---
# <span data-ttu-id="d1387-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d1387-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="d1387-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1387-102">SYNOPSIS</span></span>
<span data-ttu-id="d1387-103">Alkalmazás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="d1387-103">Remove an application from the cluster.</span></span> <span data-ttu-id="d1387-104">Ezzel eltávolítja a program az alkalmazás alatti összes szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d1387-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="d1387-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1387-105">SYNTAX</span></span>

### <span data-ttu-id="d1387-106">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1387-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1387-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1387-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1387-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1387-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1387-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1387-109">DESCRIPTION</span></span>
<span data-ttu-id="d1387-110">Ez a parancsmag eltávolítja a fürtöt az alkalmazás-űrlapok közül.</span><span class="sxs-lookup"><span data-stu-id="d1387-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="d1387-111">Ekkor az alkalmazás erőforrása alatt távolítsa el az összes szolgáltatást (ha van ilyen).</span><span class="sxs-lookup"><span data-stu-id="d1387-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="d1387-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d1387-112">EXAMPLES</span></span>

### <span data-ttu-id="d1387-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d1387-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="d1387-114">Ez a példa eltávolítja az "testApp" alkalmazást a "testRG" erőforráscsoport és a cluster "testCluster" erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="d1387-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="d1387-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1387-115">PARAMETERS</span></span>

### <span data-ttu-id="d1387-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="d1387-116">-ClusterName</span></span>
<span data-ttu-id="d1387-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="d1387-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d1387-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1387-118">-DefaultProfile</span></span>
<span data-ttu-id="d1387-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1387-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1387-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d1387-120">-Force</span></span>
<span data-ttu-id="d1387-121">Eltávolítás kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="d1387-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="d1387-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1387-122">-InputObject</span></span>
<span data-ttu-id="d1387-123">Az alkalmazás-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="d1387-123">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1387-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1387-124">-Name</span></span>
<span data-ttu-id="d1387-125">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="d1387-125">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1387-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1387-126">-PassThru</span></span>
<span data-ttu-id="d1387-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d1387-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d1387-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1387-128">-ResourceGroupName</span></span>
<span data-ttu-id="d1387-129">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="d1387-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d1387-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1387-130">-ResourceId</span></span>
<span data-ttu-id="d1387-131">A kar ResourceId az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="d1387-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="d1387-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1387-132">-Confirm</span></span>
<span data-ttu-id="d1387-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1387-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1387-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1387-134">-WhatIf</span></span>
<span data-ttu-id="d1387-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1387-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1387-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1387-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1387-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1387-137">CommonParameters</span></span>
<span data-ttu-id="d1387-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1387-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1387-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d1387-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1387-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1387-140">INPUTS</span></span>

### <span data-ttu-id="d1387-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d1387-141">System.String</span></span>

### <span data-ttu-id="d1387-142">Microsoft. Azure. Command. ServiceFabric. models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d1387-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d1387-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1387-143">OUTPUTS</span></span>

### <span data-ttu-id="d1387-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1387-144">System.Boolean</span></span>

## <span data-ttu-id="d1387-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1387-145">NOTES</span></span>

## <span data-ttu-id="d1387-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1387-146">RELATED LINKS</span></span>