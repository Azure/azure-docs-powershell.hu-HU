---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 38f7d6780b598606d0a0938178309ed67e602315
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926577"
---
# <span data-ttu-id="7348a-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7348a-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="7348a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7348a-102">SYNOPSIS</span></span>
<span data-ttu-id="7348a-103">Egy hálózati felület hatékony hálózati biztonsági csoportját használja.</span><span class="sxs-lookup"><span data-stu-id="7348a-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="7348a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7348a-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7348a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7348a-105">DESCRIPTION</span></span>
<span data-ttu-id="7348a-106">A **Get-AzEffectiveNetworkSecurityGroup** parancsmag a hálózati felületen alkalmazott hatékony hálózatbiztonsági csoportot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="7348a-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="7348a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7348a-107">EXAMPLES</span></span>

### <span data-ttu-id="7348a-108">1. példa: A hatékony hálózatbiztonsági csoport kiépítése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="7348a-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="7348a-109">Ez a parancs a MyNetworkInterface nevű hálózati felülettel társított összes hatékony hálózati biztonsági szabályt megkapja a myResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7348a-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="7348a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7348a-110">PARAMETERS</span></span>

### <span data-ttu-id="7348a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7348a-111">-DefaultProfile</span></span>
<span data-ttu-id="7348a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7348a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7348a-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7348a-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="7348a-114">A hálózati felület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7348a-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="7348a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7348a-115">-ResourceGroupName</span></span>
<span data-ttu-id="7348a-116">Egy hálózati felület erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7348a-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="7348a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7348a-117">CommonParameters</span></span>
<span data-ttu-id="7348a-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7348a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7348a-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7348a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7348a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7348a-120">INPUTS</span></span>

### <span data-ttu-id="7348a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7348a-121">System.String</span></span>

## <span data-ttu-id="7348a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7348a-122">OUTPUTS</span></span>

### <span data-ttu-id="7348a-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7348a-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="7348a-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7348a-124">NOTES</span></span>

## <span data-ttu-id="7348a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7348a-125">RELATED LINKS</span></span>

[<span data-ttu-id="7348a-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7348a-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


