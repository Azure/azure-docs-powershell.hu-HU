---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147971"
---
# <span data-ttu-id="703f5-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="703f5-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="703f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="703f5-102">SYNOPSIS</span></span>
<span data-ttu-id="703f5-103">Frissíti a DNS-rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="703f5-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="703f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="703f5-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="703f5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="703f5-105">DESCRIPTION</span></span>
<span data-ttu-id="703f5-106">A **Set-AzDnsRecordSet** parancsmag egy helyi **RecordSet-objektumból** frissíti az Azure DNS-szolgáltatás egyik rekordkészletét.</span><span class="sxs-lookup"><span data-stu-id="703f5-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="703f5-107">A **RecordSet-objektumokat** paraméterként vagy a folyamat műveleti jelének használatával is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="703f5-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="703f5-108">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="703f5-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="703f5-109">A rekordkészlet nem frissül, ha módosult az Azure DNS-ben a helyi **RecordSet** objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="703f5-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="703f5-110">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="703f5-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="703f5-111">Ezt a viselkedést  letilthatja a Felülírás paraméter használatával, amely a rekordkészletet frissíti, függetlenül a párhuzamos módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="703f5-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="703f5-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="703f5-112">EXAMPLES</span></span>

### <span data-ttu-id="703f5-113">1. példa: Rekordkészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="703f5-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="703f5-114">Az első parancs a Get-AzDnsRecordSet parancsmag használatával begyűjte a megadott rekordkészletet, majd a $RecordSet tárolja.</span><span class="sxs-lookup"><span data-stu-id="703f5-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="703f5-115">A második és a harmadik parancs off-line művelet, amely két A rekordot ad a rekordkészlethez.</span><span class="sxs-lookup"><span data-stu-id="703f5-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="703f5-116">Az utolsó parancs a **Set-AzDnsRecordSet** parancsmagot használja a frissítés véglegesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="703f5-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="703f5-117">2. példa: SOA rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="703f5-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="703f5-118">Az első parancs **a Get-AzDnsRecordset** parancsmag használatával begyűjte a megadott rekordkészletet, majd tárolja azt a $RecordSet változóban.</span><span class="sxs-lookup"><span data-stu-id="703f5-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="703f5-119">A második parancs frissíti a megadott SOA rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="703f5-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="703f5-120">Az utolsó parancs a **Set-AzDnsRecordSet** parancsmag segítségével propagálja a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="703f5-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="703f5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="703f5-121">PARAMETERS</span></span>

### <span data-ttu-id="703f5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703f5-122">-DefaultProfile</span></span>
<span data-ttu-id="703f5-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="703f5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="703f5-124">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="703f5-124">-Overwrite</span></span>
<span data-ttu-id="703f5-125">Azt jelzi, hogy frissíteni kell a rekordkészletet az egyidejű módosításoktól függetlenül.</span><span class="sxs-lookup"><span data-stu-id="703f5-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="703f5-126">A rekordkészlet nem frissül, ha módosult az Azure DNS-ben a helyi **RecordSet** objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="703f5-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="703f5-127">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="703f5-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="703f5-128">Ennek a viselkedésnek a  letiltásához használhatja a Felülírás paramétert, így a rekordkészlet frissül, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="703f5-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="703f5-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="703f5-129">-RecordSet</span></span>
<span data-ttu-id="703f5-130">A **frissítenie kell rekordkészletet** adja meg.</span><span class="sxs-lookup"><span data-stu-id="703f5-130">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="703f5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="703f5-131">-Confirm</span></span>
<span data-ttu-id="703f5-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="703f5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="703f5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="703f5-133">-WhatIf</span></span>
<span data-ttu-id="703f5-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="703f5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="703f5-135">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="703f5-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="703f5-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="703f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="703f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703f5-137">CommonParameters</span></span>
<span data-ttu-id="703f5-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="703f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703f5-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="703f5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703f5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="703f5-140">INPUTS</span></span>

### <span data-ttu-id="703f5-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="703f5-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="703f5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="703f5-142">OUTPUTS</span></span>

### <span data-ttu-id="703f5-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="703f5-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="703f5-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="703f5-144">NOTES</span></span>
<span data-ttu-id="703f5-145">A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="703f5-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="703f5-146">A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.</span><span class="sxs-lookup"><span data-stu-id="703f5-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="703f5-147">Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="703f5-147">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="703f5-148">Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="703f5-148">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="703f5-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="703f5-149">RELATED LINKS</span></span>

[<span data-ttu-id="703f5-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="703f5-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="703f5-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="703f5-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="703f5-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="703f5-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
