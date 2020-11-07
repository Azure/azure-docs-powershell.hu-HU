---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a960d5b2f6daf19fc4e46eb253b596eb88e6bd71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841682"
---
# <span data-ttu-id="b8255-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8255-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="b8255-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8255-102">SYNOPSIS</span></span>
<span data-ttu-id="b8255-103">Egy hálózati kapcsolat hatékony hálózati biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="b8255-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="b8255-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8255-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8255-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8255-105">DESCRIPTION</span></span>
<span data-ttu-id="b8255-106">A **Get-AzEffectiveNetworkSecurityGroup** parancsmag a hálózati felületen alkalmazott hatékony hálózati biztonsági csoportot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b8255-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="b8255-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b8255-107">EXAMPLES</span></span>

### <span data-ttu-id="b8255-108">Példa 1: a hatékony hálózat biztonsági csoportjának beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="b8255-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="b8255-109">Ez a parancs a myResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati csatolóval társított összes hatékony hálózati biztonsági szabályt megkapja.</span><span class="sxs-lookup"><span data-stu-id="b8255-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="b8255-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8255-110">PARAMETERS</span></span>

### <span data-ttu-id="b8255-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8255-111">-DefaultProfile</span></span>
<span data-ttu-id="b8255-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8255-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8255-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b8255-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="b8255-114">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="b8255-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="b8255-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8255-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8255-116">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8255-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="b8255-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8255-117">CommonParameters</span></span>
<span data-ttu-id="b8255-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8255-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8255-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8255-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8255-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8255-120">INPUTS</span></span>

## <span data-ttu-id="b8255-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8255-121">OUTPUTS</span></span>

### <span data-ttu-id="b8255-122">Microsoft. Azure. commands. Network. models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8255-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="b8255-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8255-123">NOTES</span></span>

## <span data-ttu-id="b8255-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8255-124">RELATED LINKS</span></span>

[<span data-ttu-id="b8255-125">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b8255-125">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


