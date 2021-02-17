---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169355"
---
# <span data-ttu-id="64860-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64860-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="64860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64860-102">SYNOPSIS</span></span>
<span data-ttu-id="64860-103">Privát DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="64860-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="64860-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64860-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64860-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64860-105">DESCRIPTION</span></span>
<span data-ttu-id="64860-106">A **Get-AzPrivateDnsZone** parancsmag egy DNS-zónát kap a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="64860-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="64860-107">Ha megadja a *Name paramétert,* a visszaadott érték egyetlen **PrivateDnsZone-objektum** lesz.</span><span class="sxs-lookup"><span data-stu-id="64860-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="64860-108">Ha nem adja meg a *Name* paramétert, a visszaadott érték egy tömb, amely a megadott erőforráscsoport összes zónáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64860-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="64860-109">A **PrivateDnsZone** objektummal frissítheti a zónát, például **RecordSet-objektumokat** adhat hozzá.</span><span class="sxs-lookup"><span data-stu-id="64860-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="64860-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64860-110">EXAMPLES</span></span>

### <span data-ttu-id="64860-111">1. példa: Zóna lekérte</span><span class="sxs-lookup"><span data-stu-id="64860-111">Example 1: Get a zone</span></span>
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

### <span data-ttu-id="64860-112">2. példa: Erőforráscsoport összes zónája</span><span class="sxs-lookup"><span data-stu-id="64860-112">Example 2: Get all of the zones in a resource group</span></span>
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

<span data-ttu-id="64860-113">Ez a példa a megadott erőforráscsoport összes privát DNS-zónáját beveszi, majd a $Zones tárolja.</span><span class="sxs-lookup"><span data-stu-id="64860-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="64860-114">3. példa: Az előfizetés összes zónája</span><span class="sxs-lookup"><span data-stu-id="64860-114">Example 3: Get all of the zones in a subscription</span></span>
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

<span data-ttu-id="64860-115">Ez a példa az aktuális Azure-előfizetés összes privát DNS-zónáját beveszi, majd a $Zones tárolja.</span><span class="sxs-lookup"><span data-stu-id="64860-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="64860-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64860-116">PARAMETERS</span></span>

### <span data-ttu-id="64860-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64860-117">-DefaultProfile</span></span>
<span data-ttu-id="64860-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="64860-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64860-119">-Name</span><span class="sxs-lookup"><span data-stu-id="64860-119">-Name</span></span>
<span data-ttu-id="64860-120">A lekért privát DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="64860-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="64860-121">Ha nem ad meg értéket a *Name* paraméternek, ez a parancsmag a megadott erőforráscsoport összes privát DNS-zónáját beveszi.</span><span class="sxs-lookup"><span data-stu-id="64860-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="64860-122">Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetés összes privát DNS-zónáját megkapja.</span><span class="sxs-lookup"><span data-stu-id="64860-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="64860-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64860-123">-ResourceGroupName</span></span>
<span data-ttu-id="64860-124">Annak az erőforráscsoportnak a neve, amely a behozni kívánt privát DNS-zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64860-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="64860-125">Ha nem adja meg az *ResourceGroupName* paramétert, akkor a *Name* paramétert is ki kell kihagyni.</span><span class="sxs-lookup"><span data-stu-id="64860-125">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="64860-126">Ebben az esetben ez a parancsmag az aktuális Azure-előfizetés összes privát DNS-zónáját beveszi.</span><span class="sxs-lookup"><span data-stu-id="64860-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="64860-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64860-127">CommonParameters</span></span>
<span data-ttu-id="64860-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64860-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64860-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64860-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64860-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64860-130">INPUTS</span></span>

### <span data-ttu-id="64860-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="64860-131">None</span></span>

## <span data-ttu-id="64860-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64860-132">OUTPUTS</span></span>

### <span data-ttu-id="64860-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64860-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="64860-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64860-134">NOTES</span></span>

## <span data-ttu-id="64860-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64860-135">RELATED LINKS</span></span>

[<span data-ttu-id="64860-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64860-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="64860-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64860-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="64860-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64860-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
