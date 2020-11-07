---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a7c131db8ce5a3489bc2a869e31b0ef7ab89f3c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673014"
---
# <span data-ttu-id="033f4-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="033f4-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="033f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="033f4-102">SYNOPSIS</span></span>
<span data-ttu-id="033f4-103">Egy hálózati kapcsolat hatékony hálózati biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="033f4-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="033f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="033f4-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="033f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="033f4-105">DESCRIPTION</span></span>
<span data-ttu-id="033f4-106">A **Get-AzureRmEffectiveNetworkSecurityGroup** parancsmag a hálózati felületen alkalmazott hatékony hálózati biztonsági csoportot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="033f4-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="033f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="033f4-107">EXAMPLES</span></span>

### <span data-ttu-id="033f4-108">Példa 1: a hatékony hálózat biztonsági csoportjának beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="033f4-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="033f4-109">Ez a parancs a myResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati csatolóval társított összes hatékony hálózati biztonsági szabályt megkapja.</span><span class="sxs-lookup"><span data-stu-id="033f4-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="033f4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="033f4-110">PARAMETERS</span></span>

### <span data-ttu-id="033f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033f4-111">-DefaultProfile</span></span>
<span data-ttu-id="033f4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="033f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033f4-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="033f4-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="033f4-114">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="033f4-114">Specified the name of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="033f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="033f4-116">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="033f4-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033f4-117">CommonParameters</span></span>
<span data-ttu-id="033f4-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="033f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033f4-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="033f4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033f4-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="033f4-120">INPUTS</span></span>

### <span data-ttu-id="033f4-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="033f4-121">None</span></span>
<span data-ttu-id="033f4-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="033f4-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="033f4-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="033f4-123">OUTPUTS</span></span>

### <span data-ttu-id="033f4-124">Microsoft. Azure. commands. Network. models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="033f4-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="033f4-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="033f4-125">NOTES</span></span>

## <span data-ttu-id="033f4-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="033f4-126">RELATED LINKS</span></span>

[<span data-ttu-id="033f4-127">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="033f4-127">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


