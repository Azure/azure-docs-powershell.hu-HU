---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024446"
---
# <span data-ttu-id="faeba-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="faeba-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="faeba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="faeba-102">SYNOPSIS</span></span>
<span data-ttu-id="faeba-103">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="faeba-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="faeba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="faeba-104">SYNTAX</span></span>

### <span data-ttu-id="faeba-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="faeba-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faeba-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="faeba-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faeba-107">ByName</span><span class="sxs-lookup"><span data-stu-id="faeba-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faeba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="faeba-108">DESCRIPTION</span></span>
<span data-ttu-id="faeba-109">A **Get-AzServiceFabricCluster** a fürterőforrás adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="faeba-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="faeba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="faeba-110">EXAMPLES</span></span>

### <span data-ttu-id="faeba-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="faeba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="faeba-112">Ez a parancs megjeleníti a cluster resource details "myCluster" adatait.</span><span class="sxs-lookup"><span data-stu-id="faeba-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="faeba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="faeba-113">PARAMETERS</span></span>

### <span data-ttu-id="faeba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faeba-114">-DefaultProfile</span></span>
<span data-ttu-id="faeba-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="faeba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faeba-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="faeba-116">-Name</span></span>
<span data-ttu-id="faeba-117">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="faeba-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="faeba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faeba-118">-ResourceGroupName</span></span>
<span data-ttu-id="faeba-119">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="faeba-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="faeba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faeba-120">CommonParameters</span></span>
<span data-ttu-id="faeba-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="faeba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faeba-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="faeba-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faeba-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="faeba-123">INPUTS</span></span>

### <span data-ttu-id="faeba-124">System. String</span><span class="sxs-lookup"><span data-stu-id="faeba-124">System.String</span></span>

## <span data-ttu-id="faeba-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="faeba-125">OUTPUTS</span></span>

### <span data-ttu-id="faeba-126">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="faeba-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="faeba-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="faeba-127">NOTES</span></span>

## <span data-ttu-id="faeba-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="faeba-128">RELATED LINKS</span></span>
