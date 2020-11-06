---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 565d0748104e537f448a40116a48f0cd34ebf16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493646"
---
# <span data-ttu-id="cea29-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cea29-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="cea29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cea29-102">SYNOPSIS</span></span>
<span data-ttu-id="cea29-103">Egy hálózati kapcsolat hatékony hálózati biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="cea29-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cea29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cea29-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cea29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cea29-105">DESCRIPTION</span></span>
<span data-ttu-id="cea29-106">A **Get-AzureRmEffectiveNetworkSecurityGroup** parancsmag a hálózati felületen alkalmazott hatékony hálózati biztonsági csoportot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="cea29-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="cea29-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cea29-107">EXAMPLES</span></span>

### <span data-ttu-id="cea29-108">Példa 1: a hatékony hálózat biztonsági csoportjának beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="cea29-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="cea29-109">Ez a parancs a myResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati csatolóval társított összes hatékony hálózati biztonsági szabályt megkapja.</span><span class="sxs-lookup"><span data-stu-id="cea29-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="cea29-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cea29-110">PARAMETERS</span></span>

### <span data-ttu-id="cea29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea29-111">-DefaultProfile</span></span>
<span data-ttu-id="cea29-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cea29-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cea29-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="cea29-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="cea29-114">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="cea29-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="cea29-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea29-115">-ResourceGroupName</span></span>
<span data-ttu-id="cea29-116">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cea29-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="cea29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea29-117">CommonParameters</span></span>
<span data-ttu-id="cea29-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cea29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea29-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea29-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea29-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cea29-120">INPUTS</span></span>

### <span data-ttu-id="cea29-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cea29-121">System.String</span></span>

## <span data-ttu-id="cea29-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cea29-122">OUTPUTS</span></span>

### <span data-ttu-id="cea29-123">Microsoft. Azure. commands. Network. models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cea29-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="cea29-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cea29-124">NOTES</span></span>

## <span data-ttu-id="cea29-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cea29-125">RELATED LINKS</span></span>

[<span data-ttu-id="cea29-126">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="cea29-126">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


