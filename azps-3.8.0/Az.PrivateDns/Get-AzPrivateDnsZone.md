---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846174"
---
# <span data-ttu-id="2576d-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2576d-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="2576d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2576d-102">SYNOPSIS</span></span>
<span data-ttu-id="2576d-103">Privát DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="2576d-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="2576d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2576d-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2576d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2576d-105">DESCRIPTION</span></span>
<span data-ttu-id="2576d-106">A **Get-AzPrivateDnsZone** parancsmag a megadott erőforráscsoport privát tartománynévrendszer (DNS) zónáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2576d-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="2576d-107">Ha a *Name* paramétert adja meg, a program egyetlen **PrivateDnsZone** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="2576d-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="2576d-108">Ha nem adja meg a *Name* paramétert, a függvény a megadott erőforráscsoport összes zónáját tartalmazó tömböt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="2576d-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="2576d-109">A **PrivateDnsZone** objektum segítségével frissítheti a zónát, például megadhatja a **rekordhalmaz** objektumait.</span><span class="sxs-lookup"><span data-stu-id="2576d-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="2576d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2576d-110">EXAMPLES</span></span>

### <span data-ttu-id="2576d-111">Példa 1: zóna beszerzése</span><span class="sxs-lookup"><span data-stu-id="2576d-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="2576d-112">2. példa: egy erőforráscsoport összes zónájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="2576d-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="2576d-113">Ez a példa a megadott erőforráscsoport minden titkos DNS-zónáját beilleszti, majd a $Zones változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2576d-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="2576d-114">3. példa: az előfizetésben szereplő összes zóna lekérése</span><span class="sxs-lookup"><span data-stu-id="2576d-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="2576d-115">Ez a példa beilleszti az aktuális Azure-előfizetéshez tartozó összes magánhálózati DNS-zónát, és a $Zones változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="2576d-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="2576d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2576d-116">PARAMETERS</span></span>

### <span data-ttu-id="2576d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2576d-117">-DefaultProfile</span></span>
<span data-ttu-id="2576d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2576d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2576d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2576d-119">-Name</span></span>
<span data-ttu-id="2576d-120">A beolvasott magánhálózati DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2576d-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="2576d-121">Ha nem ad meg értéket a *Name* paraméterhez, ez a parancsmag minden titkos DNS-zónát kap a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="2576d-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="2576d-122">Ha a *ResourceGroupName* paramétert is kihagyja, a parancsmag az aktuális Azure-előfizetésben minden titkos DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="2576d-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2576d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2576d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2576d-124">Annak a csoportnak a neve, amely a magánjellegű DNS-zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2576d-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="2576d-125">Ha nem adja meg a *ResourceGroupName* , akkor a *Name* paramétert is el kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="2576d-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="2576d-126">Ebben az esetben ez a parancsmag az aktuális Azure-előfizetésben minden titkos DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="2576d-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2576d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2576d-127">CommonParameters</span></span>
<span data-ttu-id="2576d-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2576d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2576d-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2576d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2576d-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2576d-130">INPUTS</span></span>

### <span data-ttu-id="2576d-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="2576d-131">None</span></span>

## <span data-ttu-id="2576d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2576d-132">OUTPUTS</span></span>

### <span data-ttu-id="2576d-133">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2576d-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="2576d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2576d-134">NOTES</span></span>

## <span data-ttu-id="2576d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2576d-135">RELATED LINKS</span></span>

[<span data-ttu-id="2576d-136">Új – AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2576d-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="2576d-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2576d-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="2576d-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2576d-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
