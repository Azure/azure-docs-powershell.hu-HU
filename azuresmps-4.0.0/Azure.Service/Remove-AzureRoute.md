---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016135"
---
# <span data-ttu-id="c7885-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="c7885-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="c7885-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7885-102">SYNOPSIS</span></span>
<span data-ttu-id="c7885-103">Egy útvonal eltávolítása az útvonal-táblázatból.</span><span class="sxs-lookup"><span data-stu-id="c7885-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="c7885-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7885-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7885-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7885-105">DESCRIPTION</span></span>
<span data-ttu-id="c7885-106">A **Remove-AzureRoute** parancsmag eltávolítja az útvonalat egy útvonal-táblázatból.</span><span class="sxs-lookup"><span data-stu-id="c7885-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="c7885-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7885-107">EXAMPLES</span></span>

### <span data-ttu-id="c7885-108">1. példa: útvonal eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c7885-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="c7885-109">Ez a parancs a ApplianceRouteTable nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="c7885-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="c7885-110">A parancs átadja az útválasztási táblázatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c7885-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="c7885-111">Az aktuális parancsmag eltávolítja a InternetRoute nevű útvonalat.</span><span class="sxs-lookup"><span data-stu-id="c7885-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="c7885-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7885-112">PARAMETERS</span></span>

### <span data-ttu-id="c7885-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c7885-113">-Force</span></span>
<span data-ttu-id="c7885-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c7885-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7885-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7885-115">-Profile</span></span>
<span data-ttu-id="c7885-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c7885-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c7885-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c7885-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7885-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c7885-118">-RouteName</span></span>
<span data-ttu-id="c7885-119">A parancsmag által eltávolított új útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7885-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c7885-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c7885-120">-RouteTable</span></span>
<span data-ttu-id="c7885-121">Annak az útvonalnak a táblázatát adja meg, amelyből a parancsmag eltávolítja az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="c7885-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7885-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7885-122">CommonParameters</span></span>
<span data-ttu-id="c7885-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7885-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7885-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7885-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7885-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7885-125">INPUTS</span></span>

## <span data-ttu-id="c7885-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7885-126">OUTPUTS</span></span>

## <span data-ttu-id="c7885-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7885-127">NOTES</span></span>

## <span data-ttu-id="c7885-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7885-128">RELATED LINKS</span></span>

[<span data-ttu-id="c7885-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="c7885-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


