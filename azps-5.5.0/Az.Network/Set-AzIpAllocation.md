---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202463"
---
# <span data-ttu-id="c2751-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c2751-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="c2751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2751-102">SYNOPSIS</span></span>
<span data-ttu-id="c2751-103">Módosított IpAllocation-t ment.</span><span class="sxs-lookup"><span data-stu-id="c2751-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="c2751-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2751-104">SYNTAX</span></span>

### <span data-ttu-id="c2751-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2751-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2751-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2751-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2751-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2751-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2751-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2751-108">DESCRIPTION</span></span>
<span data-ttu-id="c2751-109">A **Set-AzIpAllocation** parancsmag frissíti az Azure IpAllocation parancsmagot</span><span class="sxs-lookup"><span data-stu-id="c2751-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="c2751-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2751-110">EXAMPLES</span></span>

### <span data-ttu-id="c2751-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2751-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="c2751-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2751-112">PARAMETERS</span></span>

### <span data-ttu-id="c2751-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2751-113">-AsJob</span></span>
<span data-ttu-id="c2751-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c2751-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2751-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2751-115">-DefaultProfile</span></span>
<span data-ttu-id="c2751-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2751-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2751-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2751-117">-InputObject</span></span>
<span data-ttu-id="c2751-118">Az IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c2751-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2751-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="c2751-119">-IpAllocationTag</span></span>
<span data-ttu-id="c2751-120">Az IP-kiosztás hozzárendelési címkéi</span><span class="sxs-lookup"><span data-stu-id="c2751-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2751-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c2751-121">-Name</span></span>
<span data-ttu-id="c2751-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c2751-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2751-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2751-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2751-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c2751-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2751-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2751-125">-ResourceId</span></span>
<span data-ttu-id="c2751-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="c2751-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2751-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2751-127">-Tag</span></span>
<span data-ttu-id="c2751-128">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="c2751-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2751-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2751-129">CommonParameters</span></span>
<span data-ttu-id="c2751-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2751-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2751-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2751-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2751-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2751-132">INPUTS</span></span>

### <span data-ttu-id="c2751-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c2751-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="c2751-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2751-134">OUTPUTS</span></span>

### <span data-ttu-id="c2751-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c2751-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="c2751-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2751-136">NOTES</span></span>

## <span data-ttu-id="c2751-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2751-137">RELATED LINKS</span></span>
