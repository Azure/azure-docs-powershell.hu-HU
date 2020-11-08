---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010947"
---
# <span data-ttu-id="7abf9-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7abf9-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="7abf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7abf9-102">SYNOPSIS</span></span>
<span data-ttu-id="7abf9-103">Frissíti a DNS-rekord halmazát.</span><span class="sxs-lookup"><span data-stu-id="7abf9-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="7abf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7abf9-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7abf9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7abf9-105">DESCRIPTION</span></span>
<span data-ttu-id="7abf9-106">A **set-AzDnsRecordSet** parancsmag egy helyi **Recordset** objektumról frissíti az Azure DNS szolgáltatásban lévő rekordot.</span><span class="sxs-lookup"><span data-stu-id="7abf9-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="7abf9-107">A **rekordhalmaz** -objektum paraméterként vagy a pipeline operátor segítségével átadható.</span><span class="sxs-lookup"><span data-stu-id="7abf9-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="7abf9-108">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7abf9-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7abf9-109">A Record set nem frissül, ha az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="7abf9-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="7abf9-110">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="7abf9-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="7abf9-111">Ezt a működést a *felülírás* paraméterrel szüntetheti meg, amely az egyidejű módosításoktól függetlenül frissíti a rekordot.</span><span class="sxs-lookup"><span data-stu-id="7abf9-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="7abf9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7abf9-112">EXAMPLES</span></span>

### <span data-ttu-id="7abf9-113">Példa 1: rekordazonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="7abf9-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="7abf9-114">Az első parancs az Get-AzDnsRecordSet parancsmagot használja a megadott rekordtípus beolvasásához, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7abf9-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="7abf9-115">A második és a harmadik parancs az off-line műveletekkel két rekordot hozhat létre a rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="7abf9-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="7abf9-116">A végleges parancs a **set-AzDnsRecordSet** parancsmagot használja a frissítés véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="7abf9-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="7abf9-117">2. példa: SOA rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="7abf9-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="7abf9-118">Az első parancs a **Get-AzDnsRecordset** parancsmagot használja a megadott rekordtípus beolvasásához, majd a $Recordset változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7abf9-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="7abf9-119">A második parancs frissíti a megadott SOA-rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="7abf9-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="7abf9-120">A végleges parancs a **set-AzDnsRecordSet** parancsmagot használja a frissítés $Recordset propagálásához.</span><span class="sxs-lookup"><span data-stu-id="7abf9-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="7abf9-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7abf9-121">PARAMETERS</span></span>

### <span data-ttu-id="7abf9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abf9-122">-DefaultProfile</span></span>
<span data-ttu-id="7abf9-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7abf9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7abf9-124">-Átír</span><span class="sxs-lookup"><span data-stu-id="7abf9-124">-Overwrite</span></span>
<span data-ttu-id="7abf9-125">Azt jelzi, hogy a rekordot az egyidejű módosításoktól függetlenül frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="7abf9-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="7abf9-126">Ha a rendszer az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását, a program nem frissíti a rekordot.</span><span class="sxs-lookup"><span data-stu-id="7abf9-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="7abf9-127">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="7abf9-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="7abf9-128">Ha el szeretné tiltani ezt a problémát, használhatja a *felülírás* paramétert, amely a rekord egyidejű módosítástól függetlenül frissül.</span><span class="sxs-lookup"><span data-stu-id="7abf9-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7abf9-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="7abf9-129">-RecordSet</span></span>
<span data-ttu-id="7abf9-130">A frissítendő **rekordhalmazt** adja meg.</span><span class="sxs-lookup"><span data-stu-id="7abf9-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7abf9-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7abf9-131">-Confirm</span></span>
<span data-ttu-id="7abf9-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7abf9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7abf9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abf9-133">-WhatIf</span></span>
<span data-ttu-id="7abf9-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7abf9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7abf9-135">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7abf9-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7abf9-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7abf9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7abf9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abf9-137">CommonParameters</span></span>
<span data-ttu-id="7abf9-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7abf9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abf9-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abf9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abf9-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7abf9-140">INPUTS</span></span>

### <span data-ttu-id="7abf9-141">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7abf9-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="7abf9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7abf9-142">OUTPUTS</span></span>

### <span data-ttu-id="7abf9-143">Microsoft. Azure. Command. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7abf9-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="7abf9-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7abf9-144">NOTES</span></span>
<span data-ttu-id="7abf9-145">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7abf9-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7abf9-146">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="7abf9-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="7abf9-147">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7abf9-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="7abf9-148">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7abf9-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="7abf9-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7abf9-149">RELATED LINKS</span></span>

[<span data-ttu-id="7abf9-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7abf9-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="7abf9-151">Új – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7abf9-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="7abf9-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7abf9-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
