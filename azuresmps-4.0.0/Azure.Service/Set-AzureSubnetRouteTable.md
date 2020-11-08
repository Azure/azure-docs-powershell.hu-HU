---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015812"
---
# <span data-ttu-id="29a51-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="29a51-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="29a51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29a51-102">SYNOPSIS</span></span>
<span data-ttu-id="29a51-103">Egy útválasztási táblázatot társít az alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="29a51-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="29a51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29a51-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="29a51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29a51-105">DESCRIPTION</span></span>
<span data-ttu-id="29a51-106">A **set-AzureSubnetRouteTable** parancsmag egy útválasztási táblázatot társít az alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="29a51-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="29a51-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29a51-107">EXAMPLES</span></span>

### <span data-ttu-id="29a51-108">1. példa: az útválasztási táblázat társítása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="29a51-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="29a51-109">Ez a parancs társítja a PublicRouteTable nevű Route táblát a ContosoSubnet nevű alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="29a51-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="29a51-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29a51-110">PARAMETERS</span></span>

### <span data-ttu-id="29a51-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29a51-111">-PassThru</span></span>
<span data-ttu-id="29a51-112">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="29a51-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29a51-113">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="29a51-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29a51-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="29a51-114">-Profile</span></span>
<span data-ttu-id="29a51-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="29a51-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29a51-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="29a51-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29a51-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="29a51-117">-RouteTableName</span></span>
<span data-ttu-id="29a51-118">Annak az útválasztási táblának a nevét adja meg, amelyre a parancsmag társít egy alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="29a51-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="29a51-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="29a51-119">-SubnetName</span></span>
<span data-ttu-id="29a51-120">Azt az alhálózatot adja meg, amelyhez ez a parancsmag az útválasztási táblázatot társítja.</span><span class="sxs-lookup"><span data-stu-id="29a51-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="29a51-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="29a51-121">-VirtualNetworkName</span></span>
<span data-ttu-id="29a51-122">Megadja annak a virtuális hálózatnak a nevét, amely azt az alhálózatot tartalmazza, amelyhez ez a parancsmag az útválasztási táblázatot társítja.</span><span class="sxs-lookup"><span data-stu-id="29a51-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="29a51-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a51-123">CommonParameters</span></span>
<span data-ttu-id="29a51-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29a51-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a51-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a51-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a51-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29a51-126">INPUTS</span></span>

## <span data-ttu-id="29a51-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29a51-127">OUTPUTS</span></span>

## <span data-ttu-id="29a51-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29a51-128">NOTES</span></span>

## <span data-ttu-id="29a51-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29a51-129">RELATED LINKS</span></span>

[<span data-ttu-id="29a51-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="29a51-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="29a51-131">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="29a51-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
