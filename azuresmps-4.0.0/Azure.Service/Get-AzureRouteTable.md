---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016313"
---
# <span data-ttu-id="50b89-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="50b89-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="50b89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50b89-102">SYNOPSIS</span></span>
<span data-ttu-id="50b89-103">Beolvassa az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="50b89-103">Gets a route table.</span></span>

## <span data-ttu-id="50b89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50b89-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="50b89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50b89-105">DESCRIPTION</span></span>
<span data-ttu-id="50b89-106">A **Get-AzureRouteTable** parancsmag egy útválasztási táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="50b89-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="50b89-107">Adja meg az útválasztási táblázat útvonalait felsoroló *részletes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="50b89-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="50b89-108">Példák</span><span class="sxs-lookup"><span data-stu-id="50b89-108">EXAMPLES</span></span>

### <span data-ttu-id="50b89-109">Példa 1: az útvonaltervezés részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="50b89-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="50b89-110">Ez a parancs a ApplianceRouteTable nevű útvonalkártya adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="50b89-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="50b89-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50b89-111">PARAMETERS</span></span>

### <span data-ttu-id="50b89-112">– Részletes</span><span class="sxs-lookup"><span data-stu-id="50b89-112">-Detailed</span></span>
<span data-ttu-id="50b89-113">Azt jelzi, hogy ez a parancsmag az útválasztási táblázat útvonalait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="50b89-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="50b89-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50b89-114">-Name</span></span>
<span data-ttu-id="50b89-115">Annak az útvonal-táblázatnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="50b89-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="50b89-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="50b89-116">-Profile</span></span>
<span data-ttu-id="50b89-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="50b89-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="50b89-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="50b89-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50b89-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b89-119">CommonParameters</span></span>
<span data-ttu-id="50b89-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50b89-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b89-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b89-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b89-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50b89-122">INPUTS</span></span>

## <span data-ttu-id="50b89-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50b89-123">OUTPUTS</span></span>

## <span data-ttu-id="50b89-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50b89-124">NOTES</span></span>

## <span data-ttu-id="50b89-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50b89-125">RELATED LINKS</span></span>

[<span data-ttu-id="50b89-126">Új – AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="50b89-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="50b89-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="50b89-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


