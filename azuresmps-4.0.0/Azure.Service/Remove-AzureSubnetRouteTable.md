---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016456"
---
# <span data-ttu-id="1f9e5-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="1f9e5-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="1f9e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9e5-103">Az útválasztási táblázat társítását távolítja el az alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="1f9e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f9e5-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1f9e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f9e5-105">DESCRIPTION</span></span>
<span data-ttu-id="1f9e5-106">A **Remove-AzureSubnetRouteTable** parancsmag eltávolítja az útválasztási táblázat társítását egy alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="1f9e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f9e5-107">EXAMPLES</span></span>

### <span data-ttu-id="1f9e5-108">1. példa: az útválasztási táblázat és az alhálózat közötti társítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1f9e5-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="1f9e5-109">Ez a parancs eltávolítja a PublicRouteTable nevű útvonal-tábla társítását a ContosoSubnet nevű alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="1f9e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f9e5-110">PARAMETERS</span></span>

### <span data-ttu-id="1f9e5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1f9e5-111">-Force</span></span>
<span data-ttu-id="1f9e5-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f9e5-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f9e5-113">-PassThru</span></span>
<span data-ttu-id="1f9e5-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="1f9e5-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f9e5-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="1f9e5-116">-Profile</span></span>
<span data-ttu-id="1f9e5-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1f9e5-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f9e5-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1f9e5-119">-SubnetName</span></span>
<span data-ttu-id="1f9e5-120">Azt az alhálózatot adja meg, amelyre ez a parancsmag eltávolítja az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="1f9e5-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1f9e5-121">-VirtualNetworkName</span></span>
<span data-ttu-id="1f9e5-122">Megadja annak a virtuális hálózatnak a nevét, amely azt az alhálózatot tartalmazza, amelynek a parancsmagja eltávolítja az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="1f9e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9e5-123">CommonParameters</span></span>
<span data-ttu-id="1f9e5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f9e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9e5-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9e5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f9e5-126">INPUTS</span></span>

## <span data-ttu-id="1f9e5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f9e5-127">OUTPUTS</span></span>

## <span data-ttu-id="1f9e5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f9e5-128">NOTES</span></span>

## <span data-ttu-id="1f9e5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f9e5-129">RELATED LINKS</span></span>

[<span data-ttu-id="1f9e5-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="1f9e5-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="1f9e5-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="1f9e5-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


