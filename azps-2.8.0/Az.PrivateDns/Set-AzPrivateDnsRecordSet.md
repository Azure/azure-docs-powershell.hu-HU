---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c4f76b9731e82bd134be7ae38461a7d74e31e6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838654"
---
# <span data-ttu-id="c7e8a-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c7e8a-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="c7e8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e8a-103">Frissítések/rekordok beállítása privát DNS-zónában.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="c7e8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7e8a-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7e8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7e8a-105">DESCRIPTION</span></span>
<span data-ttu-id="c7e8a-106">Az Set-AzPrivateDnsRecordSet parancsmag egy helyi RecordSet objektumból frissíti az Azure Private DNS szolgáltatásban lévő rekordot.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="c7e8a-107">A rekordhalmaz-objektum paraméterként vagy a pipeline operátor segítségével átadható.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="c7e8a-108">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="c7e8a-109">A Record set nem frissül, ha az Azure Private DNS-ben módosította a helyi RecordSet objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="c7e8a-110">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="c7e8a-111">Ezt a működést a felülírás paraméterrel szüntetheti meg, amely az egyidejű módosításoktól függetlenül frissíti a rekordot.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="c7e8a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c7e8a-112">EXAMPLES</span></span>

### <span data-ttu-id="c7e8a-113">Példa 1: rekordazonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="c7e8a-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="c7e8a-114">Az első parancs az Get-AzPrivateDnsRecordSet parancsmagot használja a megadott rekordtípus beolvasásához, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="c7e8a-115">A második és a harmadik parancs az off-line műveletekkel két rekordot hozhat létre a rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="c7e8a-116">A végleges parancs a Set-AzPrivateDnsRecordSet parancsmagot használja a frissítés véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="c7e8a-117">2. példa: SOA rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="c7e8a-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="c7e8a-118">Az első parancs az Get-AzPrivateDnsRecordSet parancsmagot használja a megadott rekordtípus beolvasásához, majd a $RecordSet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="c7e8a-119">A második parancs frissíti a megadott SOA-rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="c7e8a-120">A végleges parancs a Set-AzPrivateDnsRecordSet parancsmagot használja a frissítés $RecordSet propagálásához.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="c7e8a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7e8a-121">PARAMETERS</span></span>

### <span data-ttu-id="c7e8a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e8a-122">-DefaultProfile</span></span>
<span data-ttu-id="c7e8a-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7e8a-124">-Átír</span><span class="sxs-lookup"><span data-stu-id="c7e8a-124">-Overwrite</span></span>
<span data-ttu-id="c7e8a-125">Ne használja a ETag mezőt a rekordhalmaz paraméterben az optimista párhuzamossági ellenőrzésekhez.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="c7e8a-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="c7e8a-126">-RecordSet</span></span>
<span data-ttu-id="c7e8a-127">Az a rekord, amelybe be szeretné szúrni a rekordot.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-127">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e8a-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7e8a-128">-Confirm</span></span>
<span data-ttu-id="c7e8a-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7e8a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7e8a-130">-WhatIf</span></span>
<span data-ttu-id="c7e8a-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7e8a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7e8a-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7e8a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e8a-133">CommonParameters</span></span>
<span data-ttu-id="c7e8a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7e8a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e8a-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e8a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e8a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7e8a-136">INPUTS</span></span>

### <span data-ttu-id="c7e8a-137">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c7e8a-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="c7e8a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7e8a-138">OUTPUTS</span></span>

### <span data-ttu-id="c7e8a-139">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c7e8a-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="c7e8a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7e8a-140">NOTES</span></span>

## <span data-ttu-id="c7e8a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7e8a-141">RELATED LINKS</span></span>
