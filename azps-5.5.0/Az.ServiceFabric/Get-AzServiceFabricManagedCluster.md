---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208046"
---
# <span data-ttu-id="7736c-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7736c-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="7736c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7736c-102">SYNOPSIS</span></span>
<span data-ttu-id="7736c-103">A felügyelt fürterőforrás részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="7736c-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="7736c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7736c-104">SYNTAX</span></span>

### <span data-ttu-id="7736c-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7736c-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7736c-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7736c-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7736c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7736c-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7736c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7736c-108">DESCRIPTION</span></span>
<span data-ttu-id="7736c-109">A felügyelt fürterőforrás részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="7736c-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="7736c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7736c-110">EXAMPLES</span></span>

### <span data-ttu-id="7736c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7736c-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="7736c-112">A fürt részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="7736c-112">Get cluster details.</span></span>

### <span data-ttu-id="7736c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7736c-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="7736c-114">A megadott erőforráscsoport alatti fürtök listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="7736c-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="7736c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7736c-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="7736c-116">Az aktuális előfizetés alatti fürtök listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="7736c-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="7736c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7736c-117">PARAMETERS</span></span>

### <span data-ttu-id="7736c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7736c-118">-DefaultProfile</span></span>
<span data-ttu-id="7736c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7736c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7736c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7736c-120">-Name</span></span>
<span data-ttu-id="7736c-121">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="7736c-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7736c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7736c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7736c-123">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="7736c-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7736c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7736c-124">CommonParameters</span></span>
<span data-ttu-id="7736c-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7736c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7736c-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7736c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7736c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7736c-127">INPUTS</span></span>

### <span data-ttu-id="7736c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7736c-128">System.String</span></span>

## <span data-ttu-id="7736c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7736c-129">OUTPUTS</span></span>

### <span data-ttu-id="7736c-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7736c-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="7736c-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7736c-131">NOTES</span></span>

## <span data-ttu-id="7736c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7736c-132">RELATED LINKS</span></span>
