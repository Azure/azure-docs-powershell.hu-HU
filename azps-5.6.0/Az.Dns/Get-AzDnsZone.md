---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: a788cf3638d124dac164f19171f1be89afc2e385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935058"
---
# <span data-ttu-id="239b7-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="239b7-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="239b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="239b7-102">SYNOPSIS</span></span>
<span data-ttu-id="239b7-103">DNS-zónát kap.</span><span class="sxs-lookup"><span data-stu-id="239b7-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="239b7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="239b7-104">SYNTAX</span></span>

### <span data-ttu-id="239b7-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="239b7-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="239b7-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="239b7-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="239b7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="239b7-107">DESCRIPTION</span></span>
<span data-ttu-id="239b7-108">A **Get-AzDnsZone** parancsmag egy DNS-zónát kap a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="239b7-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="239b7-109">Ha megadja a *Name paramétert,* egyetlen **DnsZone-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="239b7-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="239b7-110">Ha nem adja meg a *Name* paramétert, a visszaadott érték egy tömb, amely a megadott erőforráscsoport összes zónáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="239b7-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="239b7-111">A **DnsZone objektummal** frissítheti a zónát, például **RecordSet-objektumokat** adhat hozzá.</span><span class="sxs-lookup"><span data-stu-id="239b7-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="239b7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="239b7-112">EXAMPLES</span></span>

### <span data-ttu-id="239b7-113">1. példa: Zóna lekérte</span><span class="sxs-lookup"><span data-stu-id="239b7-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="239b7-114">Ebben a példában a megadott erőforráscsoportból myzone.com a DNS-zóna nevét, majd a $Zone tárolja.</span><span class="sxs-lookup"><span data-stu-id="239b7-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="239b7-115">2. példa: Erőforráscsoport összes zónája</span><span class="sxs-lookup"><span data-stu-id="239b7-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="239b7-116">Ez a példa a megadott erőforráscsoport összes DNS-zónáját beveszi, majd a $Zones tárolja.</span><span class="sxs-lookup"><span data-stu-id="239b7-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="239b7-117">3. példa: Az előfizetés összes zónája</span><span class="sxs-lookup"><span data-stu-id="239b7-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="239b7-118">Ez a példa beveszi az aktuális Azure-előfizetés összes DNS-zónáját, majd tárolja őket a $Zones változóban.</span><span class="sxs-lookup"><span data-stu-id="239b7-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="239b7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="239b7-119">PARAMETERS</span></span>

### <span data-ttu-id="239b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239b7-120">-DefaultProfile</span></span>
<span data-ttu-id="239b7-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="239b7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="239b7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="239b7-122">-Name</span></span>
<span data-ttu-id="239b7-123">A lekért DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="239b7-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="239b7-124">Ha nem ad meg értéket a *Name* paraméternek, ez a parancsmag a megadott erőforráscsoport összes DNS-zónáját beveszi.</span><span class="sxs-lookup"><span data-stu-id="239b7-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="239b7-125">Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetés összes DNS-zónáját megkapja.</span><span class="sxs-lookup"><span data-stu-id="239b7-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="239b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="239b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="239b7-127">Annak az erőforráscsoportnak a neve, amely a behozni kívánt DNS-zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="239b7-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="239b7-128">Ha nem adja meg az *ResourceGroupName* paramétert, akkor a *Name* paramétert is ki kell kihagyni.</span><span class="sxs-lookup"><span data-stu-id="239b7-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="239b7-129">Ebben az esetben ez a parancsmag az aktuális Azure-előfizetés összes DNS-zónáját beveszi.</span><span class="sxs-lookup"><span data-stu-id="239b7-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="239b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239b7-130">CommonParameters</span></span>
<span data-ttu-id="239b7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="239b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239b7-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="239b7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239b7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="239b7-133">INPUTS</span></span>

### <span data-ttu-id="239b7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="239b7-134">System.String</span></span>

## <span data-ttu-id="239b7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="239b7-135">OUTPUTS</span></span>

### <span data-ttu-id="239b7-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="239b7-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="239b7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="239b7-137">NOTES</span></span>

## <span data-ttu-id="239b7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="239b7-138">RELATED LINKS</span></span>

[<span data-ttu-id="239b7-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="239b7-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="239b7-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="239b7-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="239b7-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="239b7-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
