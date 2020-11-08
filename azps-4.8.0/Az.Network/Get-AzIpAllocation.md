---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184141"
---
# <span data-ttu-id="0fade-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="0fade-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="0fade-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fade-102">SYNOPSIS</span></span>
<span data-ttu-id="0fade-103">Azure IpAllocation kap.</span><span class="sxs-lookup"><span data-stu-id="0fade-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="0fade-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fade-104">SYNTAX</span></span>

### <span data-ttu-id="0fade-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fade-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fade-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fade-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fade-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fade-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fade-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fade-108">DESCRIPTION</span></span>
<span data-ttu-id="0fade-109">A **Get-AzIpAllocation** parancsmag Azure IpAllocation kap</span><span class="sxs-lookup"><span data-stu-id="0fade-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="0fade-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0fade-110">EXAMPLES</span></span>

### <span data-ttu-id="0fade-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fade-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="0fade-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fade-112">PARAMETERS</span></span>

### <span data-ttu-id="0fade-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fade-113">-DefaultProfile</span></span>
<span data-ttu-id="0fade-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fade-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fade-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fade-115">-Name</span></span>
<span data-ttu-id="0fade-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0fade-116">The resource name.</span></span>

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

### <span data-ttu-id="0fade-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fade-117">-ResourceGroupName</span></span>
<span data-ttu-id="0fade-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fade-118">The resource group name.</span></span>

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

### <span data-ttu-id="0fade-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fade-119">-ResourceId</span></span>
<span data-ttu-id="0fade-120">IpAllocation-azonosító</span><span class="sxs-lookup"><span data-stu-id="0fade-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="0fade-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fade-121">CommonParameters</span></span>
<span data-ttu-id="0fade-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fade-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fade-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fade-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fade-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fade-124">INPUTS</span></span>

### <span data-ttu-id="0fade-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0fade-125">System.String</span></span>

## <span data-ttu-id="0fade-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fade-126">OUTPUTS</span></span>

### <span data-ttu-id="0fade-127">Microsoft. Azure. commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="0fade-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="0fade-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fade-128">NOTES</span></span>

## <span data-ttu-id="0fade-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fade-129">RELATED LINKS</span></span>
