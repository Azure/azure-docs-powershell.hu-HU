---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024437"
---
# <span data-ttu-id="d6509-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d6509-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="d6509-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6509-102">SYNOPSIS</span></span>
<span data-ttu-id="d6509-103">Kapja meg a felügyelt fürterőforrás adatait.</span><span class="sxs-lookup"><span data-stu-id="d6509-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="d6509-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6509-104">SYNTAX</span></span>

### <span data-ttu-id="d6509-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6509-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6509-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6509-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6509-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d6509-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6509-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6509-108">DESCRIPTION</span></span>
<span data-ttu-id="d6509-109">Kapja meg a felügyelt fürterőforrás adatait.</span><span class="sxs-lookup"><span data-stu-id="d6509-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="d6509-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d6509-110">EXAMPLES</span></span>

### <span data-ttu-id="d6509-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6509-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="d6509-112">A fürtök részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="d6509-112">Get cluster details.</span></span>

### <span data-ttu-id="d6509-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d6509-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="d6509-114">A megadott erőforráscsoport alatti fürtök listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d6509-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="d6509-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d6509-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="d6509-116">A jelenlegi előfizetés alatti fürtök listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d6509-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="d6509-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6509-117">PARAMETERS</span></span>

### <span data-ttu-id="d6509-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6509-118">-DefaultProfile</span></span>
<span data-ttu-id="d6509-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6509-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6509-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6509-120">-Name</span></span>
<span data-ttu-id="d6509-121">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="d6509-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d6509-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6509-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6509-123">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="d6509-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d6509-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6509-124">CommonParameters</span></span>
<span data-ttu-id="d6509-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6509-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6509-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6509-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6509-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6509-127">INPUTS</span></span>

### <span data-ttu-id="d6509-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d6509-128">System.String</span></span>

## <span data-ttu-id="d6509-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6509-129">OUTPUTS</span></span>

### <span data-ttu-id="d6509-130">Microsoft. Azure. Command. ServiceFabric. models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d6509-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d6509-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6509-131">NOTES</span></span>

## <span data-ttu-id="d6509-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6509-132">RELATED LINKS</span></span>
