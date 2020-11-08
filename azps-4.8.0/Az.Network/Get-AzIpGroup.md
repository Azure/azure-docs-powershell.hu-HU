---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184138"
---
# <span data-ttu-id="67b30-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="67b30-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="67b30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67b30-102">SYNOPSIS</span></span>
<span data-ttu-id="67b30-103">Azure-IpGroup beszerzése</span><span class="sxs-lookup"><span data-stu-id="67b30-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="67b30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67b30-104">SYNTAX</span></span>

### <span data-ttu-id="67b30-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b30-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67b30-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b30-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67b30-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="67b30-107">DESCRIPTION</span></span>
<span data-ttu-id="67b30-108">A **Get-AzIpGroup** parancsmag Azure IpGroup kap</span><span class="sxs-lookup"><span data-stu-id="67b30-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="67b30-109">Példák</span><span class="sxs-lookup"><span data-stu-id="67b30-109">EXAMPLES</span></span>

### <span data-ttu-id="67b30-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="67b30-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="67b30-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="67b30-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="67b30-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67b30-112">PARAMETERS</span></span>

### <span data-ttu-id="67b30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b30-113">-DefaultProfile</span></span>
<span data-ttu-id="67b30-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67b30-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b30-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67b30-115">-Name</span></span>
<span data-ttu-id="67b30-116">A ipgroup neve.</span><span class="sxs-lookup"><span data-stu-id="67b30-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b30-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b30-117">-ResourceGroupName</span></span>
<span data-ttu-id="67b30-118">A ipgroup erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67b30-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b30-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67b30-119">-ResourceId</span></span>
<span data-ttu-id="67b30-120">A ipgroup ResourceId</span><span class="sxs-lookup"><span data-stu-id="67b30-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b30-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b30-121">CommonParameters</span></span>
<span data-ttu-id="67b30-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67b30-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b30-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67b30-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b30-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67b30-124">INPUTS</span></span>

### <span data-ttu-id="67b30-125">System. String</span><span class="sxs-lookup"><span data-stu-id="67b30-125">System.String</span></span>

## <span data-ttu-id="67b30-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67b30-126">OUTPUTS</span></span>

### <span data-ttu-id="67b30-127">Microsoft. Azure. commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="67b30-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="67b30-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67b30-128">NOTES</span></span>

## <span data-ttu-id="67b30-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67b30-129">RELATED LINKS</span></span>
