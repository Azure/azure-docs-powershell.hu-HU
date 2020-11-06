---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493013"
---
# <span data-ttu-id="cde7a-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cde7a-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="cde7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cde7a-102">SYNOPSIS</span></span>
<span data-ttu-id="cde7a-103">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="cde7a-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cde7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cde7a-104">SYNTAX</span></span>

### <span data-ttu-id="cde7a-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cde7a-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cde7a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cde7a-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cde7a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="cde7a-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde7a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cde7a-108">DESCRIPTION</span></span>
<span data-ttu-id="cde7a-109">A **AzureRmServiceFabricCluster** a cluster resource adatait fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="cde7a-109">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="cde7a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cde7a-110">EXAMPLES</span></span>

### <span data-ttu-id="cde7a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cde7a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="cde7a-112">Ez a parancs megjeleníti a cluster resource details "myCluster" adatait.</span><span class="sxs-lookup"><span data-stu-id="cde7a-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="cde7a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cde7a-113">PARAMETERS</span></span>

### <span data-ttu-id="cde7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde7a-114">-DefaultProfile</span></span>
<span data-ttu-id="cde7a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cde7a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde7a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cde7a-116">-Name</span></span>
<span data-ttu-id="cde7a-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="cde7a-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde7a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde7a-118">-ResourceGroupName</span></span>
<span data-ttu-id="cde7a-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cde7a-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde7a-120">CommonParameters</span></span>
<span data-ttu-id="cde7a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cde7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde7a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde7a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde7a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cde7a-123">INPUTS</span></span>

### <span data-ttu-id="cde7a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cde7a-124">System.String</span></span>

## <span data-ttu-id="cde7a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cde7a-125">OUTPUTS</span></span>

### <span data-ttu-id="cde7a-126">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ServiceFabric. models. PsCluster, Microsoft. Azure. commands. ServiceFabric, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cde7a-126">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cde7a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cde7a-127">NOTES</span></span>

## <span data-ttu-id="cde7a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cde7a-128">RELATED LINKS</span></span>

