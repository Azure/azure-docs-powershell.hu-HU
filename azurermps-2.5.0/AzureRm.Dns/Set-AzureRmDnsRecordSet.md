---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c6479f9358322ae76eeb2fdf3cb9f2bb922e462
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848850"
---
# <span data-ttu-id="d6a72-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6a72-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="d6a72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6a72-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a72-103">Frissíti a DNS-rekord halmazát.</span><span class="sxs-lookup"><span data-stu-id="d6a72-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6a72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6a72-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6a72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6a72-105">DESCRIPTION</span></span>
<span data-ttu-id="d6a72-106">A **set-AzureRmDnsRecordSet** parancsmag egy helyi **Recordset** objektumról frissíti az Azure DNS szolgáltatásban lévő rekordot.</span><span class="sxs-lookup"><span data-stu-id="d6a72-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="d6a72-107">A **rekordhalmaz** -objektum paraméterként vagy a pipeline operátor segítségével átadható.</span><span class="sxs-lookup"><span data-stu-id="d6a72-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="d6a72-108">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6a72-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="d6a72-109">A Record set nem frissül, ha az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="d6a72-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d6a72-110">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="d6a72-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d6a72-111">Ezt a működést a *felülírás* paraméterrel szüntetheti meg, amely az egyidejű módosításoktól függetlenül frissíti a rekordot.</span><span class="sxs-lookup"><span data-stu-id="d6a72-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d6a72-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d6a72-112">EXAMPLES</span></span>

### <span data-ttu-id="d6a72-113">Példa 1: rekordazonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="d6a72-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="d6a72-114">Az első parancs az Get-AzureRmDnsRecordSet parancsmagot használja a megadott rekordtípus beolvasásához, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6a72-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="d6a72-115">A második és a harmadik parancs az off-line műveletekkel két rekordot hozhat létre a rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="d6a72-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="d6a72-116">A végleges parancs a **set-AzureRmDnsRecordSet** parancsmagot használja a frissítés véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d6a72-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="d6a72-117">2. példa: SOA rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="d6a72-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="d6a72-118">Az első parancs a **Get-AzureRmDnsRecordset** parancsmagot használja a megadott rekordtípus beolvasásához, majd a $Recordset változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6a72-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="d6a72-119">A második parancs frissíti a megadott SOA-rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d6a72-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="d6a72-120">A végleges parancs a **set-AzureRmDnsRecordSet** parancsmagot használja a frissítés $Recordset propagálásához.</span><span class="sxs-lookup"><span data-stu-id="d6a72-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="d6a72-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6a72-121">PARAMETERS</span></span>

### <span data-ttu-id="d6a72-122">-Átír</span><span class="sxs-lookup"><span data-stu-id="d6a72-122">-Overwrite</span></span>
<span data-ttu-id="d6a72-123">Azt jelzi, hogy a rekordot az egyidejű módosításoktól függetlenül frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="d6a72-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="d6a72-124">Ha a rendszer az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását, a program nem frissíti a rekordot.</span><span class="sxs-lookup"><span data-stu-id="d6a72-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d6a72-125">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="d6a72-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d6a72-126">Ha el szeretné tiltani ezt a problémát, használhatja a *felülírás* paramétert, amely a rekord egyidejű módosítástól függetlenül frissül.</span><span class="sxs-lookup"><span data-stu-id="d6a72-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d6a72-127">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="d6a72-127">-RecordSet</span></span>
<span data-ttu-id="d6a72-128">A frissítendő **rekordhalmazt** adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6a72-128">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a72-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6a72-129">-Confirm</span></span>
<span data-ttu-id="d6a72-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6a72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6a72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a72-131">-WhatIf</span></span>
<span data-ttu-id="d6a72-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6a72-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6a72-133">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6a72-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6a72-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6a72-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6a72-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a72-135">CommonParameters</span></span>
<span data-ttu-id="d6a72-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6a72-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a72-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a72-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a72-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a72-138">INPUTS</span></span>

### <span data-ttu-id="d6a72-139">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6a72-139">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="d6a72-140">A **Recordset** objektum átadható a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d6a72-140">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="d6a72-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a72-141">OUTPUTS</span></span>

### <span data-ttu-id="d6a72-142">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6a72-142">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="d6a72-143">Ez a parancsmag egy olyan objektumot ad eredményül, amely a frissített **Recordset** objektumot jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d6a72-143">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="d6a72-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6a72-144">NOTES</span></span>
<span data-ttu-id="d6a72-145">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6a72-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d6a72-146">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="d6a72-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="d6a72-147">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6a72-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d6a72-148">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6a72-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="d6a72-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6a72-149">RELATED LINKS</span></span>

[<span data-ttu-id="d6a72-150">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6a72-150">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d6a72-151">Új – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6a72-151">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d6a72-152">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6a72-152">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
