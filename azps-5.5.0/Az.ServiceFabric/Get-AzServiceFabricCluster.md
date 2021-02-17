---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165075"
---
# <span data-ttu-id="4b1df-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4b1df-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="4b1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b1df-102">SYNOPSIS</span></span>
<span data-ttu-id="4b1df-103">A fürterőforrás részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="4b1df-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="4b1df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b1df-104">SYNTAX</span></span>

### <span data-ttu-id="4b1df-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b1df-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b1df-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4b1df-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b1df-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4b1df-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b1df-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b1df-108">DESCRIPTION</span></span>
<span data-ttu-id="4b1df-109">A **Get-AzServiceFabricCluster** le fogja kapni a fürterőforrás részleteit.</span><span class="sxs-lookup"><span data-stu-id="4b1df-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="4b1df-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b1df-110">EXAMPLES</span></span>

### <span data-ttu-id="4b1df-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4b1df-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="4b1df-112">Ez a parancs be fogja szerezni a "myCluster" fürt erőforrásának részleteit.</span><span class="sxs-lookup"><span data-stu-id="4b1df-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="4b1df-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b1df-113">PARAMETERS</span></span>

### <span data-ttu-id="4b1df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1df-114">-DefaultProfile</span></span>
<span data-ttu-id="4b1df-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b1df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b1df-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4b1df-116">-Name</span></span>
<span data-ttu-id="4b1df-117">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="4b1df-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4b1df-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b1df-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b1df-119">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="4b1df-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4b1df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1df-120">CommonParameters</span></span>
<span data-ttu-id="4b1df-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b1df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1df-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b1df-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1df-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b1df-123">INPUTS</span></span>

### <span data-ttu-id="4b1df-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4b1df-124">System.String</span></span>

## <span data-ttu-id="4b1df-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b1df-125">OUTPUTS</span></span>

### <span data-ttu-id="4b1df-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="4b1df-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4b1df-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b1df-127">NOTES</span></span>

## <span data-ttu-id="4b1df-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b1df-128">RELATED LINKS</span></span>
