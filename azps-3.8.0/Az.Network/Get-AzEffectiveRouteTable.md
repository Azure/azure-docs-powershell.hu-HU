---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014867"
---
# <span data-ttu-id="f4ce7-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4ce7-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="f4ce7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ce7-103">Beilleszti egy hálózati kapcsolat tényleges útválasztási táblázatát.</span><span class="sxs-lookup"><span data-stu-id="f4ce7-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="f4ce7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4ce7-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ce7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ce7-106">A **Get-AzEffectiveRouteTable** parancsmag a hálózati felületen alkalmazott tényleges útválasztási táblázatot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f4ce7-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="f4ce7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="f4ce7-108">Példa 1: a tényleges Route-táblázat beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="f4ce7-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f4ce7-109">Ez a parancs a MyResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati kapcsolattal társított tényleges útvonali táblát kapja.</span><span class="sxs-lookup"><span data-stu-id="f4ce7-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f4ce7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4ce7-110">PARAMETERS</span></span>

### <span data-ttu-id="f4ce7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4ce7-111">-AsJob</span></span>
<span data-ttu-id="f4ce7-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f4ce7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4ce7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ce7-113">-DefaultProfile</span></span>
<span data-ttu-id="f4ce7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4ce7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ce7-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f4ce7-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="f4ce7-116">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="f4ce7-116">Specified the name of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ce7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ce7-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4ce7-118">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ce7-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ce7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ce7-119">CommonParameters</span></span>
<span data-ttu-id="f4ce7-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4ce7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ce7-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4ce7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ce7-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ce7-122">INPUTS</span></span>

### <span data-ttu-id="f4ce7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ce7-123">System.String</span></span>

## <span data-ttu-id="f4ce7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ce7-124">OUTPUTS</span></span>

### <span data-ttu-id="f4ce7-125">Microsoft. Azure. commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="f4ce7-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="f4ce7-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4ce7-126">NOTES</span></span>

## <span data-ttu-id="f4ce7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4ce7-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4ce7-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f4ce7-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


