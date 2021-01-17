---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479996"
---
# <span data-ttu-id="c2a06-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c2a06-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="c2a06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2a06-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a06-103">Azure IpAllocation-t kap.</span><span class="sxs-lookup"><span data-stu-id="c2a06-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="c2a06-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2a06-104">SYNTAX</span></span>

### <span data-ttu-id="c2a06-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a06-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a06-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a06-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a06-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a06-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2a06-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2a06-108">DESCRIPTION</span></span>
<span data-ttu-id="c2a06-109">A **Get-AzIpAllocation** parancsmag egy Azure IpAllocation-t kap</span><span class="sxs-lookup"><span data-stu-id="c2a06-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="c2a06-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2a06-110">EXAMPLES</span></span>

### <span data-ttu-id="c2a06-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2a06-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="c2a06-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2a06-112">PARAMETERS</span></span>

### <span data-ttu-id="c2a06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a06-113">-DefaultProfile</span></span>
<span data-ttu-id="c2a06-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2a06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a06-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c2a06-115">-Name</span></span>
<span data-ttu-id="c2a06-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c2a06-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a06-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2a06-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c2a06-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a06-119">-ResourceId</span></span>
<span data-ttu-id="c2a06-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="c2a06-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a06-121">CommonParameters</span></span>
<span data-ttu-id="c2a06-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a06-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a06-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2a06-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a06-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2a06-124">INPUTS</span></span>

### <span data-ttu-id="c2a06-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c2a06-125">System.String</span></span>

## <span data-ttu-id="c2a06-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2a06-126">OUTPUTS</span></span>

### <span data-ttu-id="c2a06-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c2a06-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="c2a06-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2a06-128">NOTES</span></span>

## <span data-ttu-id="c2a06-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2a06-129">RELATED LINKS</span></span>
