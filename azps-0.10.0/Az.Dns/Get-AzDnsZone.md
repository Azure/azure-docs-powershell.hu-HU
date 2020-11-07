---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844018"
---
# <span data-ttu-id="29336-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="29336-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="29336-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29336-102">SYNOPSIS</span></span>
<span data-ttu-id="29336-103">DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="29336-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="29336-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29336-104">SYNTAX</span></span>

### <span data-ttu-id="29336-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29336-105">Default (Default)</span></span>
```
Get-AzDnsZone [<CommonParameters>]
```

### <span data-ttu-id="29336-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29336-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="29336-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29336-107">DESCRIPTION</span></span>
<span data-ttu-id="29336-108">A **Get-AzDnsZone** parancsmag a megadott erőforráscsoport tartománynévrendszer (DNS) zónájába kerül.</span><span class="sxs-lookup"><span data-stu-id="29336-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="29336-109">Ha a *Name* paramétert adja meg, a program egyetlen **dnsZone** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="29336-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="29336-110">Ha nem adja meg a *Name* paramétert, a függvény a megadott erőforráscsoport összes zónáját tartalmazó tömböt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="29336-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="29336-111">A **dnsZone** objektum segítségével frissítheti a zónát, például megadhatja a **rekordhalmaz** objektumait.</span><span class="sxs-lookup"><span data-stu-id="29336-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="29336-112">Példák</span><span class="sxs-lookup"><span data-stu-id="29336-112">EXAMPLES</span></span>

### <span data-ttu-id="29336-113">Példa 1: zóna beszerzése</span><span class="sxs-lookup"><span data-stu-id="29336-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="29336-114">Ebben a példában a myzone.com nevű DNS-zónát kapja meg a megadott erőforráscsoport, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="29336-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="29336-115">2. példa: egy erőforráscsoport összes zónájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="29336-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="29336-116">Ez a példa a megadott erőforráscsoport összes DNS-zónáját beilleszti, majd a $Zones változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="29336-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="29336-117">3. példa: az előfizetésben szereplő összes zóna lekérése</span><span class="sxs-lookup"><span data-stu-id="29336-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="29336-118">Ez a példa beilleszti az összes DNS-zónát az aktuális Azure-előfizetésbe, majd a $Zones változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="29336-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="29336-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29336-119">PARAMETERS</span></span>

### <span data-ttu-id="29336-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29336-120">-Name</span></span>
<span data-ttu-id="29336-121">A beszerzéshez használandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29336-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="29336-122">Ha nem ad meg értéket a *Name* paraméterhez, ez a parancsmag a megadott erőforráscsoport összes DNS-zónáját megkapja.</span><span class="sxs-lookup"><span data-stu-id="29336-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="29336-123">Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetésből az összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="29336-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="29336-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29336-124">-ResourceGroupName</span></span>
<span data-ttu-id="29336-125">A beszerzéshez használt DNS-zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29336-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="29336-126">Ha nem adja meg a *ResourceGroupName* , akkor a *Name* paramétert is el kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="29336-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="29336-127">Ebben az esetben ez a parancsmag a jelenlegi Azure-előfizetésben lévő összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="29336-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="29336-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29336-128">CommonParameters</span></span>
<span data-ttu-id="29336-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29336-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29336-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29336-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29336-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29336-131">INPUTS</span></span>

### <span data-ttu-id="29336-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="29336-132">None</span></span>
<span data-ttu-id="29336-133">Ez a parancsmag nem teszi lehetővé a pipe-bevitelt.</span><span class="sxs-lookup"><span data-stu-id="29336-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="29336-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29336-134">OUTPUTS</span></span>

### <span data-ttu-id="29336-135">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="29336-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="29336-136">Ez a parancsmag egy olyan objektumot ad eredményül, amely a DNS-zónát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="29336-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="29336-137">Ha a zóna neve nincs megadva, a program a zóna-objektumok tömbjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="29336-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="29336-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29336-138">NOTES</span></span>

## <span data-ttu-id="29336-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29336-139">RELATED LINKS</span></span>

[<span data-ttu-id="29336-140">Új – AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="29336-140">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="29336-141">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="29336-141">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="29336-142">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="29336-142">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
