---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 9be5ca678b690400e044b9627fd455ea2cbc29c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666560"
---
# <span data-ttu-id="4ebcf-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="4ebcf-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="4ebcf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ebcf-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebcf-103">DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="4ebcf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ebcf-104">SYNTAX</span></span>

### <span data-ttu-id="4ebcf-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ebcf-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ebcf-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ebcf-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ebcf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ebcf-107">DESCRIPTION</span></span>
<span data-ttu-id="4ebcf-108">A **Get-AzDnsZone** parancsmag a megadott erőforráscsoport tartománynévrendszer (DNS) zónájába kerül.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="4ebcf-109">Ha a *Name* paramétert adja meg, a program egyetlen **dnsZone** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="4ebcf-110">Ha nem adja meg a *Name* paramétert, a függvény a megadott erőforráscsoport összes zónáját tartalmazó tömböt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="4ebcf-111">A **dnsZone** objektum segítségével frissítheti a zónát, például megadhatja a **rekordhalmaz** objektumait.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="4ebcf-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4ebcf-112">EXAMPLES</span></span>

### <span data-ttu-id="4ebcf-113">Példa 1: zóna beszerzése</span><span class="sxs-lookup"><span data-stu-id="4ebcf-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="4ebcf-114">Ebben a példában a myzone.com nevű DNS-zónát kapja meg a megadott erőforráscsoport, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="4ebcf-115">2. példa: egy erőforráscsoport összes zónájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="4ebcf-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4ebcf-116">Ez a példa a megadott erőforráscsoport összes DNS-zónáját beilleszti, majd a $Zones változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="4ebcf-117">3. példa: az előfizetésben szereplő összes zóna lekérése</span><span class="sxs-lookup"><span data-stu-id="4ebcf-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="4ebcf-118">Ez a példa beilleszti az összes DNS-zónát az aktuális Azure-előfizetésbe, majd a $Zones változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="4ebcf-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ebcf-119">PARAMETERS</span></span>

### <span data-ttu-id="4ebcf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebcf-120">-DefaultProfile</span></span>
<span data-ttu-id="4ebcf-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ebcf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ebcf-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ebcf-122">-Name</span></span>
<span data-ttu-id="4ebcf-123">A beszerzéshez használandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="4ebcf-124">Ha nem ad meg értéket a *Name* paraméterhez, ez a parancsmag a megadott erőforráscsoport összes DNS-zónáját megkapja.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="4ebcf-125">Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetésből az összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="4ebcf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebcf-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ebcf-127">A beszerzéshez használt DNS-zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="4ebcf-128">Ha nem adja meg a *ResourceGroupName* , akkor a *Name* paramétert is el kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="4ebcf-129">Ebben az esetben ez a parancsmag a jelenlegi Azure-előfizetésben lévő összes DNS-zónát megkapja.</span><span class="sxs-lookup"><span data-stu-id="4ebcf-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="4ebcf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebcf-130">CommonParameters</span></span>
<span data-ttu-id="4ebcf-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ebcf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebcf-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebcf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebcf-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ebcf-133">INPUTS</span></span>

### <span data-ttu-id="4ebcf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebcf-134">System.String</span></span>

## <span data-ttu-id="4ebcf-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ebcf-135">OUTPUTS</span></span>

### <span data-ttu-id="4ebcf-136">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="4ebcf-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="4ebcf-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ebcf-137">NOTES</span></span>

## <span data-ttu-id="4ebcf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ebcf-138">RELATED LINKS</span></span>

[<span data-ttu-id="4ebcf-139">Új – AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="4ebcf-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="4ebcf-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="4ebcf-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="4ebcf-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="4ebcf-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
