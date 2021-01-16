---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348714"
---
# <span data-ttu-id="ceb25-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ceb25-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ceb25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceb25-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb25-103">Egy privát DNS-zónában beállított rekord frissítése/beállítása.</span><span class="sxs-lookup"><span data-stu-id="ceb25-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="ceb25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ceb25-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceb25-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ceb25-105">DESCRIPTION</span></span>
<span data-ttu-id="ceb25-106">A Set-AzPrivateDnsRecordSet parancsmag egy helyi RecordSet-objektumból frissíti az Azure Private DNS szolgáltatásban beállított rekordokat.</span><span class="sxs-lookup"><span data-stu-id="ceb25-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="ceb25-107">A RecordSet-objektumokat paraméterként vagy a folyamat műveleti jelének használatával is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="ceb25-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="ceb25-108">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="ceb25-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="ceb25-109">A rekordkészlet nem frissül, ha módosult az Azure Private DNS-ben a helyi RecordSet objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="ceb25-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="ceb25-110">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="ceb25-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="ceb25-111">Ezt a viselkedést letilthatja a Felülírás paraméter használatával, amely a rekordkészletet frissíti, függetlenül a párhuzamos módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="ceb25-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="ceb25-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ceb25-112">EXAMPLES</span></span>

### <span data-ttu-id="ceb25-113">1. példa: Rekordkészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="ceb25-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="ceb25-114">Az első parancs a Get-AzPrivateDnsRecordSet parancsmag használatával begyűjte a megadott rekordkészletet, majd a $RecordSet tárolja.</span><span class="sxs-lookup"><span data-stu-id="ceb25-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="ceb25-115">A második és a harmadik parancs off-line művelet, amely két A rekordot ad a rekordkészlethez.</span><span class="sxs-lookup"><span data-stu-id="ceb25-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="ceb25-116">Az utolsó parancs a Set-AzPrivateDnsRecordSet parancsmag használatával véglegesítést ad.</span><span class="sxs-lookup"><span data-stu-id="ceb25-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="ceb25-117">2. példa: SOA rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="ceb25-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="ceb25-118">Az első parancs a Get-AzPrivateDnsRecordSet parancsmag használatával begyűjte a megadott rekordkészletet, majd a $RecordSet tárolja.</span><span class="sxs-lookup"><span data-stu-id="ceb25-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="ceb25-119">A második parancs frissíti a megadott SOA rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ceb25-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="ceb25-120">Az utolsó parancs a Set-AzPrivateDnsRecordSet parancsmag használatával propagálja a frissítést a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ceb25-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="ceb25-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceb25-121">PARAMETERS</span></span>

### <span data-ttu-id="ceb25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb25-122">-DefaultProfile</span></span>
<span data-ttu-id="ceb25-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ceb25-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceb25-124">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="ceb25-124">-Overwrite</span></span>
<span data-ttu-id="ceb25-125">Az optimista egyidejűség-ellenőrzéshez ne használja a RecordSet paraméter ETag mezőjét.</span><span class="sxs-lookup"><span data-stu-id="ceb25-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="ceb25-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="ceb25-126">-RecordSet</span></span>
<span data-ttu-id="ceb25-127">Az a rekordkészlet, amelyben hozzá kell adni a rekordot.</span><span class="sxs-lookup"><span data-stu-id="ceb25-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="ceb25-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceb25-128">-Confirm</span></span>
<span data-ttu-id="ceb25-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ceb25-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceb25-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceb25-130">-WhatIf</span></span>
<span data-ttu-id="ceb25-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ceb25-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceb25-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ceb25-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceb25-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb25-133">CommonParameters</span></span>
<span data-ttu-id="ceb25-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb25-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb25-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb25-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb25-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ceb25-136">INPUTS</span></span>

### <span data-ttu-id="ceb25-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ceb25-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ceb25-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceb25-138">OUTPUTS</span></span>

### <span data-ttu-id="ceb25-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ceb25-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ceb25-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ceb25-140">NOTES</span></span>

## <span data-ttu-id="ceb25-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceb25-141">RELATED LINKS</span></span>
