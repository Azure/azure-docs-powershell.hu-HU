---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024548"
---
# <span data-ttu-id="53707-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="53707-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="53707-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53707-102">SYNOPSIS</span></span>
<span data-ttu-id="53707-103">Módosított IpAllocation mentése</span><span class="sxs-lookup"><span data-stu-id="53707-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="53707-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53707-104">SYNTAX</span></span>

### <span data-ttu-id="53707-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53707-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53707-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53707-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53707-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53707-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53707-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="53707-108">DESCRIPTION</span></span>
<span data-ttu-id="53707-109">A **set-AzIpAllocation** parancsmag egy Azure-IpAllocation frissít</span><span class="sxs-lookup"><span data-stu-id="53707-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="53707-110">Példák</span><span class="sxs-lookup"><span data-stu-id="53707-110">EXAMPLES</span></span>

### <span data-ttu-id="53707-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="53707-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="53707-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53707-112">PARAMETERS</span></span>

### <span data-ttu-id="53707-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53707-113">-AsJob</span></span>
<span data-ttu-id="53707-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="53707-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53707-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53707-115">-DefaultProfile</span></span>
<span data-ttu-id="53707-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53707-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53707-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53707-117">-InputObject</span></span>
<span data-ttu-id="53707-118">A IpAllocation</span><span class="sxs-lookup"><span data-stu-id="53707-118">The IpAllocation</span></span>

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

### <span data-ttu-id="53707-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="53707-119">-IpAllocationTag</span></span>
<span data-ttu-id="53707-120">Az IP-kiosztás kiosztási címkéi</span><span class="sxs-lookup"><span data-stu-id="53707-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="53707-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53707-121">-Name</span></span>
<span data-ttu-id="53707-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="53707-122">The resource name.</span></span>

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

### <span data-ttu-id="53707-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53707-123">-ResourceGroupName</span></span>
<span data-ttu-id="53707-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="53707-124">The resource group name.</span></span>

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

### <span data-ttu-id="53707-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53707-125">-ResourceId</span></span>
<span data-ttu-id="53707-126">IpAllocation-azonosító</span><span class="sxs-lookup"><span data-stu-id="53707-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="53707-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="53707-127">-Tag</span></span>
<span data-ttu-id="53707-128">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="53707-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="53707-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53707-129">CommonParameters</span></span>
<span data-ttu-id="53707-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53707-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53707-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="53707-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53707-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53707-132">INPUTS</span></span>

### <span data-ttu-id="53707-133">Microsoft. Azure. commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="53707-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="53707-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53707-134">OUTPUTS</span></span>

### <span data-ttu-id="53707-135">Microsoft. Azure. commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="53707-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="53707-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53707-136">NOTES</span></span>

## <span data-ttu-id="53707-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53707-137">RELATED LINKS</span></span>
