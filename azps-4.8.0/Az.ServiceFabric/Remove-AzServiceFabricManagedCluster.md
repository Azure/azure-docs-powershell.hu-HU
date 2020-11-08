---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183307"
---
# <span data-ttu-id="9cc0e-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="9cc0e-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="9cc0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cc0e-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc0e-103">Fürterőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-103">Remove cluster resource.</span></span>

## <span data-ttu-id="9cc0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cc0e-104">SYNTAX</span></span>

### <span data-ttu-id="9cc0e-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cc0e-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc0e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9cc0e-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc0e-107">ById</span><span class="sxs-lookup"><span data-stu-id="9cc0e-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc0e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cc0e-108">DESCRIPTION</span></span>
<span data-ttu-id="9cc0e-109">Fürt eltávolítása: ezzel a beállítással eltávolíthatja a csomópont típusait a fürtben.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="9cc0e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9cc0e-110">EXAMPLES</span></span>

### <span data-ttu-id="9cc0e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9cc0e-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="9cc0e-112">Fürt eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-112">Remove cluster.</span></span>

### <span data-ttu-id="9cc0e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9cc0e-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="9cc0e-114">A fürtök eltávolítása a csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="9cc0e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cc0e-115">PARAMETERS</span></span>

### <span data-ttu-id="9cc0e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cc0e-116">-AsJob</span></span>
<span data-ttu-id="9cc0e-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9cc0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc0e-118">-DefaultProfile</span></span>
<span data-ttu-id="9cc0e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cc0e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cc0e-120">-InputObject</span></span>
<span data-ttu-id="9cc0e-121">Felügyelt cluster resource</span><span class="sxs-lookup"><span data-stu-id="9cc0e-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc0e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cc0e-122">-Name</span></span>
<span data-ttu-id="9cc0e-123">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc0e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cc0e-124">-PassThru</span></span>
<span data-ttu-id="9cc0e-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9cc0e-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9cc0e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc0e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9cc0e-127">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc0e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cc0e-128">-ResourceId</span></span>
<span data-ttu-id="9cc0e-129">Felügyelt cluster resource azonosító</span><span class="sxs-lookup"><span data-stu-id="9cc0e-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc0e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cc0e-130">-Confirm</span></span>
<span data-ttu-id="9cc0e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc0e-132">-WhatIf</span></span>
<span data-ttu-id="9cc0e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc0e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc0e-135">CommonParameters</span></span>
<span data-ttu-id="9cc0e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cc0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc0e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9cc0e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc0e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc0e-138">INPUTS</span></span>

### <span data-ttu-id="9cc0e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc0e-139">System.String</span></span>

## <span data-ttu-id="9cc0e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc0e-140">OUTPUTS</span></span>

### <span data-ttu-id="9cc0e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cc0e-141">System.Boolean</span></span>

## <span data-ttu-id="9cc0e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cc0e-142">NOTES</span></span>

## <span data-ttu-id="9cc0e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cc0e-143">RELATED LINKS</span></span>
