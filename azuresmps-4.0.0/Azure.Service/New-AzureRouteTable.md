---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015989"
---
# <span data-ttu-id="a2b60-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2b60-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="a2b60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2b60-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b60-103">Útválasztási táblázat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a2b60-103">Creates a route table.</span></span>

## <span data-ttu-id="a2b60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2b60-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2b60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2b60-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b60-106">A **New-AzureRouteTable** parancsmag egy útválasztási táblázatot hoz létre a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="a2b60-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="a2b60-107">Felhasználó által definiált útvonalakat adhat az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="a2b60-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="a2b60-108">Az útválasztási táblázatot társíthatja a virtuális hálózat egy alhálózatához is.</span><span class="sxs-lookup"><span data-stu-id="a2b60-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="a2b60-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a2b60-109">EXAMPLES</span></span>

## <span data-ttu-id="a2b60-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2b60-110">PARAMETERS</span></span>

### <span data-ttu-id="a2b60-111">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="a2b60-111">-Label</span></span>
<span data-ttu-id="a2b60-112">Az új útvonal-tábla leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2b60-112">Specifies a description for the new route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b60-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="a2b60-113">-Location</span></span>
<span data-ttu-id="a2b60-114">Azt a helyet adja meg, ahol ez a parancsmag hozza létre az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a2b60-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="a2b60-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2b60-115">-Name</span></span>
<span data-ttu-id="a2b60-116">A parancsmag által létrehozott útválasztási táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2b60-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a2b60-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a2b60-117">-Profile</span></span>
<span data-ttu-id="a2b60-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a2b60-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a2b60-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a2b60-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2b60-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b60-120">CommonParameters</span></span>
<span data-ttu-id="a2b60-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2b60-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b60-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b60-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b60-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2b60-123">INPUTS</span></span>

## <span data-ttu-id="a2b60-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2b60-124">OUTPUTS</span></span>

## <span data-ttu-id="a2b60-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2b60-125">NOTES</span></span>

## <span data-ttu-id="a2b60-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2b60-126">RELATED LINKS</span></span>

[<span data-ttu-id="a2b60-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2b60-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="a2b60-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2b60-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


