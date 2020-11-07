---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850022"
---
# <span data-ttu-id="a5de6-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a5de6-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="a5de6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5de6-102">SYNOPSIS</span></span>
<span data-ttu-id="a5de6-103">DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="a5de6-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5de6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5de6-104">SYNTAX</span></span>

### <span data-ttu-id="a5de6-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5de6-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="a5de6-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5de6-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="a5de6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5de6-107">DESCRIPTION</span></span>
<span data-ttu-id="a5de6-108">A **Get-AzureRmDnsZone** parancsmag a megadott erőforráscsoport tartománynévrendszer (DNS) zónájába kerül.</span><span class="sxs-lookup"><span data-stu-id="a5de6-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="a5de6-109">Ha a *Name* paramétert adja meg, a program egyetlen **dnsZone** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a5de6-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="a5de6-110">Ha nem adja meg a *Name* paramétert, a függvény a megadott erőforráscsoport összes zónáját tartalmazó tömböt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a5de6-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="a5de6-111">A **dnsZone** objektum segítségével frissítheti a zónát, például megadhatja a **rekordhalmaz** objektumait.</span><span class="sxs-lookup"><span data-stu-id="a5de6-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="a5de6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a5de6-112">EXAMPLES</span></span>

### <span data-ttu-id="a5de6-113">Példa 1: zóna beszerzése</span><span class="sxs-lookup"><span data-stu-id="a5de6-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="a5de6-114">Ebben a példában a myzone.com nevű DNS-zónát kapja meg a megadott erőforráscsoport, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5de6-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a5de6-115">2. példa: egy erőforráscsoport összes zónájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a5de6-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a5de6-116">Ez a példa a megadott erőforráscsoport összes DNS-zónáját beilleszti, majd a $Zones változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5de6-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="a5de6-117">3. példa: az előfizetésben szereplő összes zóna lekérése</span><span class="sxs-lookup"><span data-stu-id="a5de6-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="a5de6-118">Ez a példa beilleszti az összes DNS-zónát az aktuális Azure-előfizetésbe, majd a $Zones változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="a5de6-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="a5de6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5de6-119">PARAMETERS</span></span>

### <span data-ttu-id="a5de6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5de6-120">-Name</span></span>
<span data-ttu-id="a5de6-121">A beszerzéshez használandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5de6-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="a5de6-122">Ha nem ad meg értéket a *Name* paraméterhez, ez a parancsmag a megadott erőforráscsoport összes DNS-zónáját megkapja.</span><span class="sxs-lookup"><span data-stu-id="a5de6-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="a5de6-123">Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetésből az összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="a5de6-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5de6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5de6-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5de6-125">A beszerzéshez használt DNS-zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5de6-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="a5de6-126">Ha nem adja meg a *ResourceGroupName* , akkor a *Name* paramétert is el kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="a5de6-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="a5de6-127">Ebben az esetben ez a parancsmag a jelenlegi Azure-előfizetésben lévő összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="a5de6-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5de6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5de6-128">CommonParameters</span></span>
<span data-ttu-id="a5de6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5de6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5de6-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5de6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5de6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5de6-131">INPUTS</span></span>

### <span data-ttu-id="a5de6-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5de6-132">None</span></span>
<span data-ttu-id="a5de6-133">Ez a parancsmag nem teszi lehetővé a pipe-bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a5de6-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="a5de6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5de6-134">OUTPUTS</span></span>

### <span data-ttu-id="a5de6-135">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a5de6-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a5de6-136">Ez a parancsmag egy olyan objektumot ad eredményül, amely a DNS-zónát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a5de6-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="a5de6-137">Ha a zóna neve nincs megadva, a program a zóna-objektumok tömbjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a5de6-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="a5de6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5de6-138">NOTES</span></span>

## <span data-ttu-id="a5de6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5de6-139">RELATED LINKS</span></span>

[<span data-ttu-id="a5de6-140">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a5de6-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="a5de6-141">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a5de6-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="a5de6-142">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a5de6-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
