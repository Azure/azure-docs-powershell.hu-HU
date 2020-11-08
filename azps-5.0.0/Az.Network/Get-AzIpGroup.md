---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195208"
---
# <span data-ttu-id="4b530-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4b530-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="4b530-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b530-102">SYNOPSIS</span></span>
<span data-ttu-id="4b530-103">Azure-IpGroup beszerzése</span><span class="sxs-lookup"><span data-stu-id="4b530-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="4b530-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b530-104">SYNTAX</span></span>

### <span data-ttu-id="4b530-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b530-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b530-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b530-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b530-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b530-107">DESCRIPTION</span></span>
<span data-ttu-id="4b530-108">A **Get-AzIpGroup** parancsmag Azure IpGroup kap</span><span class="sxs-lookup"><span data-stu-id="4b530-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="4b530-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4b530-109">EXAMPLES</span></span>

### <span data-ttu-id="4b530-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4b530-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="4b530-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="4b530-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="4b530-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b530-112">PARAMETERS</span></span>

### <span data-ttu-id="4b530-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b530-113">-DefaultProfile</span></span>
<span data-ttu-id="4b530-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b530-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b530-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b530-115">-Name</span></span>
<span data-ttu-id="4b530-116">A ipgroup neve.</span><span class="sxs-lookup"><span data-stu-id="4b530-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="4b530-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b530-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b530-118">A ipgroup erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b530-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="4b530-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b530-119">-ResourceId</span></span>
<span data-ttu-id="4b530-120">A ipgroup ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b530-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="4b530-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b530-121">CommonParameters</span></span>
<span data-ttu-id="4b530-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b530-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b530-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4b530-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b530-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b530-124">INPUTS</span></span>

### <span data-ttu-id="4b530-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4b530-125">System.String</span></span>

## <span data-ttu-id="4b530-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b530-126">OUTPUTS</span></span>

### <span data-ttu-id="4b530-127">Microsoft. Azure. commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="4b530-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="4b530-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b530-128">NOTES</span></span>

## <span data-ttu-id="4b530-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b530-129">RELATED LINKS</span></span>
