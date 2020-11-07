---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 9d4e0e376e611e1373d30ab6b3aeafb51f363c31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679772"
---
# <span data-ttu-id="32bae-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="32bae-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="32bae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32bae-102">SYNOPSIS</span></span>
<span data-ttu-id="32bae-103">Frissíti egy DNS-zóna tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="32bae-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32bae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32bae-104">SYNTAX</span></span>

### <span data-ttu-id="32bae-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="32bae-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bae-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="32bae-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32bae-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="32bae-107">DESCRIPTION</span></span>
<span data-ttu-id="32bae-108">A **set-AzureRmDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="32bae-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="32bae-109">Ez a parancsmag nem frissíti a rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="32bae-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="32bae-110">Átadhatja a **dnsZone** -objektumokat paraméterként vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="32bae-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="32bae-111">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32bae-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="32bae-112">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="32bae-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="32bae-113">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="32bae-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="32bae-114">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="32bae-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="32bae-115">Példák</span><span class="sxs-lookup"><span data-stu-id="32bae-115">EXAMPLES</span></span>

### <span data-ttu-id="32bae-116">Példa 1: DNS-zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="32bae-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="32bae-117">Az első parancs a megadott erőforráscsoporthoz tartozó myzone.com nevű zónát kapja, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="32bae-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="32bae-118">A második parancs frissíti az $Zone címkéit.</span><span class="sxs-lookup"><span data-stu-id="32bae-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="32bae-119">A végleges parancs véglegesíti a módosítást.</span><span class="sxs-lookup"><span data-stu-id="32bae-119">The final command commits the change.</span></span>

### <span data-ttu-id="32bae-120">2. példa: a zóna címkék frissítése</span><span class="sxs-lookup"><span data-stu-id="32bae-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="32bae-121">Ez a parancs frissíti a myzone.com nevű zóna címkéit anélkül, hogy először explicit módon kapja meg a zónát.</span><span class="sxs-lookup"><span data-stu-id="32bae-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="32bae-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32bae-122">PARAMETERS</span></span>

### <span data-ttu-id="32bae-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="32bae-123">-Name</span></span>
<span data-ttu-id="32bae-124">A frissítendő DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32bae-124">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bae-125">-Átír</span><span class="sxs-lookup"><span data-stu-id="32bae-125">-Overwrite</span></span>
<span data-ttu-id="32bae-126">Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="32bae-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="32bae-127">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="32bae-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="32bae-128">Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="32bae-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bae-129">-ResourceGroupName</span></span>
<span data-ttu-id="32bae-130">A frissítendő zónát tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32bae-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="32bae-131">Meg kell adnia a ZoneName paramétert is.</span><span class="sxs-lookup"><span data-stu-id="32bae-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="32bae-132">Azt is megteheti, hogy a zónát egy DnsZone-objektummal, a *Zone* paraméterrel vagy a csővezetékkel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="32bae-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bae-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="32bae-133">-Tag</span></span>
<span data-ttu-id="32bae-134">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="32bae-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="32bae-135">Példa:</span><span class="sxs-lookup"><span data-stu-id="32bae-135">For example:</span></span>

<span data-ttu-id="32bae-136">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="32bae-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bae-137">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="32bae-137">-Zone</span></span>
<span data-ttu-id="32bae-138">A frissítendő DNS-zónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="32bae-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="32bae-139">Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.</span><span class="sxs-lookup"><span data-stu-id="32bae-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32bae-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32bae-140">-Confirm</span></span>
<span data-ttu-id="32bae-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32bae-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bae-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bae-142">-WhatIf</span></span>
<span data-ttu-id="32bae-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32bae-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32bae-144">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32bae-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32bae-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32bae-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bae-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bae-146">-DefaultProfile</span></span>
<span data-ttu-id="32bae-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32bae-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32bae-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bae-148">CommonParameters</span></span>
<span data-ttu-id="32bae-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32bae-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bae-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32bae-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bae-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32bae-151">INPUTS</span></span>

### <span data-ttu-id="32bae-152">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="32bae-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="32bae-153">Ezt a parancsmagot a DnsZone-objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="32bae-153">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="32bae-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32bae-154">OUTPUTS</span></span>

### <span data-ttu-id="32bae-155">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="32bae-155">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="32bae-156">Ez a parancsmag egy DnsZone-objektumot ad eredményül, amely a frissített DNS-zónát egy új ETAG jelképezi.</span><span class="sxs-lookup"><span data-stu-id="32bae-156">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="32bae-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32bae-157">NOTES</span></span>
<span data-ttu-id="32bae-158">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32bae-158">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="32bae-159">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="32bae-159">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="32bae-160">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32bae-160">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="32bae-161">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32bae-161">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="32bae-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32bae-162">RELATED LINKS</span></span>

[<span data-ttu-id="32bae-163">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="32bae-163">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="32bae-164">Új – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="32bae-164">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="32bae-165">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="32bae-165">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
