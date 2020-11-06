---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504728"
---
# <span data-ttu-id="482e8-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="482e8-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="482e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="482e8-102">SYNOPSIS</span></span>
<span data-ttu-id="482e8-103">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="482e8-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="482e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="482e8-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="482e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="482e8-105">DESCRIPTION</span></span>
<span data-ttu-id="482e8-106">A **AzureRmServiceFabricCluster** a cluster resource adatait fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="482e8-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="482e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="482e8-107">EXAMPLES</span></span>

### <span data-ttu-id="482e8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="482e8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="482e8-109">Ez a parancs megjeleníti a cluster resource details "myCluster" adatait.</span><span class="sxs-lookup"><span data-stu-id="482e8-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="482e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="482e8-110">PARAMETERS</span></span>

### <span data-ttu-id="482e8-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="482e8-111">-Name</span></span>
<span data-ttu-id="482e8-112">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="482e8-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482e8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="482e8-113">-ResourceGroupName</span></span>
<span data-ttu-id="482e8-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="482e8-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482e8-115">-DefaultProfile</span></span>
<span data-ttu-id="482e8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="482e8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="482e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482e8-117">CommonParameters</span></span>
<span data-ttu-id="482e8-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="482e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482e8-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="482e8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482e8-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="482e8-120">INPUTS</span></span>

### <span data-ttu-id="482e8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="482e8-121">System.String</span></span>

## <span data-ttu-id="482e8-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="482e8-122">OUTPUTS</span></span>

### <span data-ttu-id="482e8-123">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ServiceFabric. models. PsCluster, Microsoft. Azure. commands. ServiceFabric, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="482e8-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="482e8-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="482e8-124">NOTES</span></span>

## <span data-ttu-id="482e8-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="482e8-125">RELATED LINKS</span></span>

