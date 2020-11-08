---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016132"
---
# <span data-ttu-id="2e6a4-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="2e6a4-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="2e6a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6a4-103">Egy útválasztási táblázat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-103">Removes a route table.</span></span>

## <span data-ttu-id="2e6a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e6a4-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e6a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e6a4-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6a4-106">A **Remove-AzureRouteTable** parancsmag eltávolítja az útválasztási táblázatot az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="2e6a4-107">Ha egy útválasztási táblázat egy alhálózathoz van társítva, akkor nem távolíthatja el a táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="2e6a4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2e6a4-108">EXAMPLES</span></span>

### <span data-ttu-id="2e6a4-109">1. példa: a Route Table eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2e6a4-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="2e6a4-110">Ez a parancs eltávolítja a PublicRouteTable nevű útvonalkártya-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="2e6a4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e6a4-111">PARAMETERS</span></span>

### <span data-ttu-id="2e6a4-112">-Force</span><span class="sxs-lookup"><span data-stu-id="2e6a4-112">-Force</span></span>
<span data-ttu-id="2e6a4-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e6a4-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e6a4-114">-Name</span></span>
<span data-ttu-id="2e6a4-115">A parancsmag által eltávolított útválasztási táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2e6a4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e6a4-116">-PassThru</span></span>
<span data-ttu-id="2e6a4-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e6a4-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e6a4-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="2e6a4-119">-Profile</span></span>
<span data-ttu-id="2e6a4-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e6a4-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2e6a4-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e6a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6a4-122">CommonParameters</span></span>
<span data-ttu-id="2e6a4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e6a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6a4-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6a4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6a4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e6a4-125">INPUTS</span></span>

## <span data-ttu-id="2e6a4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e6a4-126">OUTPUTS</span></span>

## <span data-ttu-id="2e6a4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e6a4-127">NOTES</span></span>

## <span data-ttu-id="2e6a4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e6a4-128">RELATED LINKS</span></span>

[<span data-ttu-id="2e6a4-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="2e6a4-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="2e6a4-130">Új – AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="2e6a4-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
