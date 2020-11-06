---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: d479c66b899637f2dc12061b7499fc65b7d59d66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497820"
---
# <span data-ttu-id="f3342-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f3342-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f3342-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3342-102">SYNOPSIS</span></span>
<span data-ttu-id="f3342-103">Egy hálózati kapcsolat hatékony hálózati biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="f3342-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3342-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3342-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3342-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3342-105">DESCRIPTION</span></span>
<span data-ttu-id="f3342-106">A **Get-AzureRmEffectiveNetworkSecurityGroup** parancsmag a hálózati felületen alkalmazott hatékony hálózati biztonsági csoportot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f3342-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="f3342-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3342-107">EXAMPLES</span></span>

### <span data-ttu-id="f3342-108">Példa 1: a hatékony hálózat biztonsági csoportjának beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="f3342-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="f3342-109">Ez a parancs a myResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati csatolóval társított összes hatékony hálózati biztonsági szabályt megkapja.</span><span class="sxs-lookup"><span data-stu-id="f3342-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="f3342-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3342-110">PARAMETERS</span></span>

### <span data-ttu-id="f3342-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f3342-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="f3342-112">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="f3342-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="f3342-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3342-113">-ResourceGroupName</span></span>
<span data-ttu-id="f3342-114">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3342-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="f3342-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3342-115">-DefaultProfile</span></span>
<span data-ttu-id="f3342-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3342-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3342-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3342-117">CommonParameters</span></span>
<span data-ttu-id="f3342-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3342-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3342-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3342-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3342-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3342-120">INPUTS</span></span>

## <span data-ttu-id="f3342-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3342-121">OUTPUTS</span></span>

### <span data-ttu-id="f3342-122">Microsoft. Azure. commands. Network. models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f3342-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f3342-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3342-123">NOTES</span></span>

## <span data-ttu-id="f3342-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3342-124">RELATED LINKS</span></span>

[<span data-ttu-id="f3342-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3342-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


