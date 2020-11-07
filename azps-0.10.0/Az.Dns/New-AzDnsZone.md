---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843997"
---
# <span data-ttu-id="8dd9e-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8dd9e-101">New-AzDnsZone</span></span>

## <span data-ttu-id="8dd9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8dd9e-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd9e-103">Új DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="8dd9e-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="8dd9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8dd9e-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dd9e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8dd9e-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd9e-106">A **New-AzDnsZone** parancsmag egy új DNS-zónát hoz létre a megadott erőforráscsoport-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="8dd9e-107">Adjon meg egy egyedi DNS-zóna nevét a *Name* paraméterhez, vagy a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="8dd9e-108">A zóna létrehozása után a New-AzDnsRecordSet parancsmagot használva hozhat létre rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="8dd9e-109">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8dd9e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8dd9e-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd9e-111">Példa 1: DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="8dd9e-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8dd9e-112">Ez a parancs létrehoz egy új DNS-zónát a megadott erőforráscsoport myzone.com, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="8dd9e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8dd9e-113">PARAMETERS</span></span>

### <span data-ttu-id="8dd9e-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8dd9e-114">-Name</span></span>
<span data-ttu-id="8dd9e-115">A létrehozandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="8dd9e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd9e-116">-ResourceGroupName</span></span>
<span data-ttu-id="8dd9e-117">Azt az erőforráscsoportot adja meg, amelybe a zónát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="8dd9e-118">-Címke</span><span class="sxs-lookup"><span data-stu-id="8dd9e-118">-Tag</span></span>
<span data-ttu-id="8dd9e-119">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8dd9e-120">Példa:</span><span class="sxs-lookup"><span data-stu-id="8dd9e-120">For example:</span></span>

<span data-ttu-id="8dd9e-121">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="8dd9e-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd9e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8dd9e-122">-Confirm</span></span>
<span data-ttu-id="8dd9e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd9e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd9e-124">-WhatIf</span></span>
<span data-ttu-id="8dd9e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dd9e-126">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dd9e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd9e-128">CommonParameters</span></span>
<span data-ttu-id="8dd9e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8dd9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd9e-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd9e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd9e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dd9e-131">INPUTS</span></span>

### <span data-ttu-id="8dd9e-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="8dd9e-132">None</span></span>

<span data-ttu-id="8dd9e-133">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="8dd9e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dd9e-134">OUTPUTS</span></span>

### <span data-ttu-id="8dd9e-135">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="8dd9e-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="8dd9e-136">Ez a parancsmag az új DNS-zónát képviselő Microsoft. Azure. Command. DNS. DnsZone objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="8dd9e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8dd9e-137">NOTES</span></span>
<span data-ttu-id="8dd9e-138">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8dd9e-139">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="8dd9e-140">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8dd9e-141">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dd9e-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8dd9e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8dd9e-142">RELATED LINKS</span></span>

[<span data-ttu-id="8dd9e-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8dd9e-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="8dd9e-144">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8dd9e-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8dd9e-145">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8dd9e-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)