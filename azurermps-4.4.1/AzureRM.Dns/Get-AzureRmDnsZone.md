---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: eabf0809aebf50458d15b195a5ec9afc4f0b9cf1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679775"
---
# <span data-ttu-id="9341b-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="9341b-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="9341b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9341b-102">SYNOPSIS</span></span>
<span data-ttu-id="9341b-103">DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="9341b-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9341b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9341b-104">SYNTAX</span></span>

### <span data-ttu-id="9341b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9341b-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9341b-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9341b-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9341b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9341b-107">DESCRIPTION</span></span>
<span data-ttu-id="9341b-108">A **Get-AzureRmDnsZone** parancsmag a megadott erőforráscsoport tartománynévrendszer (DNS) zónájába kerül.</span><span class="sxs-lookup"><span data-stu-id="9341b-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="9341b-109">Ha a *Name* paramétert adja meg, a program egyetlen **dnsZone** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9341b-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="9341b-110">Ha nem adja meg a *Name* paramétert, a függvény a megadott erőforráscsoport összes zónáját tartalmazó tömböt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9341b-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="9341b-111">A **dnsZone** objektum segítségével frissítheti a zónát, például megadhatja a **rekordhalmaz** objektumait.</span><span class="sxs-lookup"><span data-stu-id="9341b-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="9341b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9341b-112">EXAMPLES</span></span>

### <span data-ttu-id="9341b-113">Példa 1: zóna beszerzése</span><span class="sxs-lookup"><span data-stu-id="9341b-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="9341b-114">Ebben a példában a myzone.com nevű DNS-zónát kapja meg a megadott erőforráscsoport, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9341b-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="9341b-115">2. példa: egy erőforráscsoport összes zónájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="9341b-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="9341b-116">Ez a példa a megadott erőforráscsoport összes DNS-zónáját beilleszti, majd a $Zones változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9341b-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="9341b-117">3. példa: az előfizetésben szereplő összes zóna lekérése</span><span class="sxs-lookup"><span data-stu-id="9341b-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="9341b-118">Ez a példa beilleszti az összes DNS-zónát az aktuális Azure-előfizetésbe, majd a $Zones változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="9341b-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="9341b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9341b-119">PARAMETERS</span></span>

### <span data-ttu-id="9341b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9341b-120">-Name</span></span>
<span data-ttu-id="9341b-121">A beszerzéshez használandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9341b-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="9341b-122">Ha nem ad meg értéket a *Name* paraméterhez, ez a parancsmag a megadott erőforráscsoport összes DNS-zónáját megkapja.</span><span class="sxs-lookup"><span data-stu-id="9341b-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="9341b-123">Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetésből az összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="9341b-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9341b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9341b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9341b-125">A beszerzéshez használt DNS-zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9341b-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="9341b-126">Ha nem adja meg a *ResourceGroupName* , akkor a *Name* paramétert is el kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="9341b-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="9341b-127">Ebben az esetben ez a parancsmag a jelenlegi Azure-előfizetésben lévő összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="9341b-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9341b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9341b-128">-DefaultProfile</span></span>
<span data-ttu-id="9341b-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9341b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9341b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9341b-130">CommonParameters</span></span>
<span data-ttu-id="9341b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9341b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9341b-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9341b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9341b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9341b-133">INPUTS</span></span>

### <span data-ttu-id="9341b-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="9341b-134">None</span></span>
<span data-ttu-id="9341b-135">Ez a parancsmag nem teszi lehetővé a pipe-bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9341b-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="9341b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9341b-136">OUTPUTS</span></span>

### <span data-ttu-id="9341b-137">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="9341b-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="9341b-138">Ez a parancsmag egy olyan objektumot ad eredményül, amely a DNS-zónát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9341b-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="9341b-139">Ha a zóna neve nincs megadva, a program a zóna-objektumok tömbjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9341b-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="9341b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9341b-140">NOTES</span></span>

## <span data-ttu-id="9341b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9341b-141">RELATED LINKS</span></span>

[<span data-ttu-id="9341b-142">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="9341b-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="9341b-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="9341b-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="9341b-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="9341b-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
