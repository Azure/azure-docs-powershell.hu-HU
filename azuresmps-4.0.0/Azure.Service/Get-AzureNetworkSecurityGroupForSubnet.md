---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015638"
---
# <span data-ttu-id="31061-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="31061-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="31061-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31061-102">SYNOPSIS</span></span>
<span data-ttu-id="31061-103">Az alhálózat hálózati biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="31061-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="31061-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31061-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="31061-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31061-105">DESCRIPTION</span></span>
<span data-ttu-id="31061-106">A **Get-AzureNetworkSecurityGroupForSubnet** parancsmag az alhálózathoz társított hálózati biztonsági csoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="31061-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="31061-107">Példák</span><span class="sxs-lookup"><span data-stu-id="31061-107">EXAMPLES</span></span>

## <span data-ttu-id="31061-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31061-108">PARAMETERS</span></span>

### <span data-ttu-id="31061-109">– Részletes</span><span class="sxs-lookup"><span data-stu-id="31061-109">-Detailed</span></span>
<span data-ttu-id="31061-110">Jelzi, hogy ez a parancsmag a hálózat biztonsági szabályait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="31061-110">Indicates that this cmdlet displays the network security rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31061-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="31061-111">-Profile</span></span>
<span data-ttu-id="31061-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="31061-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31061-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="31061-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31061-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="31061-114">-SubnetName</span></span>
<span data-ttu-id="31061-115">Annak az alhálózatnak a neve, amelyhez a parancsmag hálózati biztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="31061-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31061-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="31061-116">-VirtualNetworkName</span></span>
<span data-ttu-id="31061-117">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31061-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="31061-118">Ez a parancsmag hálózati biztonsági csoportot kap a virtuális hálózatban a virtuális hálózatban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="31061-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31061-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31061-119">CommonParameters</span></span>
<span data-ttu-id="31061-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31061-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31061-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31061-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31061-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31061-122">INPUTS</span></span>

## <span data-ttu-id="31061-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31061-123">OUTPUTS</span></span>

## <span data-ttu-id="31061-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31061-124">NOTES</span></span>

## <span data-ttu-id="31061-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31061-125">RELATED LINKS</span></span>

[<span data-ttu-id="31061-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="31061-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="31061-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="31061-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
