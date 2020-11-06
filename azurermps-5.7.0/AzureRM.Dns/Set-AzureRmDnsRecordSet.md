---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 69cdea37f0a736c13d561ecd0d6864f3ef71b466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502596"
---
# <span data-ttu-id="4f832-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f832-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="4f832-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f832-102">SYNOPSIS</span></span>
<span data-ttu-id="4f832-103">Frissíti a DNS-rekord halmazát.</span><span class="sxs-lookup"><span data-stu-id="4f832-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f832-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f832-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f832-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f832-105">DESCRIPTION</span></span>
<span data-ttu-id="4f832-106">A **set-AzureRmDnsRecordSet** parancsmag egy helyi **Recordset** objektumról frissíti az Azure DNS szolgáltatásban lévő rekordot.</span><span class="sxs-lookup"><span data-stu-id="4f832-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="4f832-107">A **rekordhalmaz** -objektum paraméterként vagy a pipeline operátor segítségével átadható.</span><span class="sxs-lookup"><span data-stu-id="4f832-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="4f832-108">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f832-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="4f832-109">A Record set nem frissül, ha az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="4f832-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4f832-110">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="4f832-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4f832-111">Ezt a működést a *felülírás* paraméterrel szüntetheti meg, amely az egyidejű módosításoktól függetlenül frissíti a rekordot.</span><span class="sxs-lookup"><span data-stu-id="4f832-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="4f832-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4f832-112">EXAMPLES</span></span>

### <span data-ttu-id="4f832-113">Példa 1: rekordazonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="4f832-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4f832-114">Az első parancs az Get-AzureRmDnsRecordSet parancsmagot használja a megadott rekordtípus beolvasásához, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4f832-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="4f832-115">A második és a harmadik parancs az off-line műveletekkel két rekordot hozhat létre a rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="4f832-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="4f832-116">A végleges parancs a **set-AzureRmDnsRecordSet** parancsmagot használja a frissítés véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="4f832-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="4f832-117">2. példa: SOA rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="4f832-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="4f832-118">Az első parancs a **Get-AzureRmDnsRecordset** parancsmagot használja a megadott rekordtípus beolvasásához, majd a $Recordset változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4f832-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="4f832-119">A második parancs frissíti a megadott SOA-rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4f832-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="4f832-120">A végleges parancs a **set-AzureRmDnsRecordSet** parancsmagot használja a frissítés $Recordset propagálásához.</span><span class="sxs-lookup"><span data-stu-id="4f832-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="4f832-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f832-121">PARAMETERS</span></span>

### <span data-ttu-id="4f832-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f832-122">-DefaultProfile</span></span>
<span data-ttu-id="4f832-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4f832-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f832-124">-Átír</span><span class="sxs-lookup"><span data-stu-id="4f832-124">-Overwrite</span></span>
<span data-ttu-id="4f832-125">Azt jelzi, hogy a rekordot az egyidejű módosításoktól függetlenül frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="4f832-125">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="4f832-126">Ha a rendszer az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását, a program nem frissíti a rekordot.</span><span class="sxs-lookup"><span data-stu-id="4f832-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4f832-127">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="4f832-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4f832-128">Ha el szeretné tiltani ezt a problémát, használhatja a *felülírás* paramétert, amely a rekord egyidejű módosítástól függetlenül frissül.</span><span class="sxs-lookup"><span data-stu-id="4f832-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4f832-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="4f832-129">-RecordSet</span></span>
<span data-ttu-id="4f832-130">A frissítendő **rekordhalmazt** adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f832-130">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="4f832-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f832-131">-Confirm</span></span>
<span data-ttu-id="4f832-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f832-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f832-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f832-133">-WhatIf</span></span>
<span data-ttu-id="4f832-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f832-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f832-135">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f832-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f832-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f832-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f832-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f832-137">CommonParameters</span></span>
<span data-ttu-id="4f832-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f832-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f832-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f832-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f832-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f832-140">INPUTS</span></span>

### <span data-ttu-id="4f832-141">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f832-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="4f832-142">A **Recordset** objektum átadható a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="4f832-142">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="4f832-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f832-143">OUTPUTS</span></span>

### <span data-ttu-id="4f832-144">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f832-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="4f832-145">Ez a parancsmag egy olyan objektumot ad eredményül, amely a frissített **Recordset** objektumot jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4f832-145">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="4f832-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f832-146">NOTES</span></span>
<span data-ttu-id="4f832-147">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f832-147">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4f832-148">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="4f832-148">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="4f832-149">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f832-149">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="4f832-150">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f832-150">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="4f832-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f832-151">RELATED LINKS</span></span>

[<span data-ttu-id="4f832-152">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f832-152">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="4f832-153">Új – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f832-153">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="4f832-154">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f832-154">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
