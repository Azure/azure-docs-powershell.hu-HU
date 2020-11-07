---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: b954c1b6c5085dd285b925d57fe0b4649830bffd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669117"
---
# <span data-ttu-id="5f3a3-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5f3a3-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="5f3a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3a3-103">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="5f3a3-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="5f3a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f3a3-104">SYNTAX</span></span>

### <span data-ttu-id="5f3a3-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f3a3-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f3a3-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f3a3-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f3a3-107">ByName</span><span class="sxs-lookup"><span data-stu-id="5f3a3-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f3a3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f3a3-108">DESCRIPTION</span></span>
<span data-ttu-id="5f3a3-109">A **Get-AzServiceFabricCluster** a fürterőforrás adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="5f3a3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5f3a3-110">EXAMPLES</span></span>

### <span data-ttu-id="5f3a3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5f3a3-111">Example 1</span></span>
```
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="5f3a3-112">Ez a parancs megjeleníti a cluster resource details "myCluster" adatait.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="5f3a3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f3a3-113">PARAMETERS</span></span>

### <span data-ttu-id="5f3a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f3a3-114">-DefaultProfile</span></span>
<span data-ttu-id="5f3a3-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f3a3-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5f3a3-116">-Name</span></span>
<span data-ttu-id="5f3a3-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5f3a3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f3a3-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f3a3-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5f3a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f3a3-120">CommonParameters</span></span>
<span data-ttu-id="5f3a3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f3a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f3a3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f3a3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f3a3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f3a3-123">INPUTS</span></span>

### <span data-ttu-id="5f3a3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5f3a3-124">System.String</span></span>

## <span data-ttu-id="5f3a3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f3a3-125">OUTPUTS</span></span>

### <span data-ttu-id="5f3a3-126">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="5f3a3-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5f3a3-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f3a3-127">NOTES</span></span>

## <span data-ttu-id="5f3a3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f3a3-128">RELATED LINKS</span></span>
