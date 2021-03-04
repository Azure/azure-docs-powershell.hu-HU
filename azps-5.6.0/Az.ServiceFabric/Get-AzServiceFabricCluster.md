---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 4695502bddb11b1b033b75057ba5ff3d2bf96b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920434"
---
# <span data-ttu-id="c7498-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c7498-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="c7498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7498-102">SYNOPSIS</span></span>
<span data-ttu-id="c7498-103">A fürterőforrás részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="c7498-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="c7498-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7498-104">SYNTAX</span></span>

### <span data-ttu-id="c7498-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7498-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7498-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7498-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7498-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c7498-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7498-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7498-108">DESCRIPTION</span></span>
<span data-ttu-id="c7498-109">A **Get-AzServiceFabricCluster** le fogja kapni a fürterőforrás részleteit.</span><span class="sxs-lookup"><span data-stu-id="c7498-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="c7498-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7498-110">EXAMPLES</span></span>

### <span data-ttu-id="c7498-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c7498-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="c7498-112">Ez a parancs be fogja szerezni a "myCluster" fürt erőforrásának részleteit.</span><span class="sxs-lookup"><span data-stu-id="c7498-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="c7498-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7498-113">PARAMETERS</span></span>

### <span data-ttu-id="c7498-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7498-114">-DefaultProfile</span></span>
<span data-ttu-id="c7498-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7498-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7498-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c7498-116">-Name</span></span>
<span data-ttu-id="c7498-117">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="c7498-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c7498-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7498-118">-ResourceGroupName</span></span>
<span data-ttu-id="c7498-119">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c7498-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c7498-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7498-120">CommonParameters</span></span>
<span data-ttu-id="c7498-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7498-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7498-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7498-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7498-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7498-123">INPUTS</span></span>

### <span data-ttu-id="c7498-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c7498-124">System.String</span></span>

## <span data-ttu-id="c7498-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7498-125">OUTPUTS</span></span>

### <span data-ttu-id="c7498-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="c7498-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c7498-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7498-127">NOTES</span></span>

## <span data-ttu-id="c7498-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7498-128">RELATED LINKS</span></span>
