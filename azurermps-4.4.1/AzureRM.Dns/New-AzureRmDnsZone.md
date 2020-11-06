---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500852"
---
# <span data-ttu-id="1116b-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1116b-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="1116b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1116b-102">SYNOPSIS</span></span>
<span data-ttu-id="1116b-103">Új DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="1116b-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1116b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1116b-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1116b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1116b-105">DESCRIPTION</span></span>
<span data-ttu-id="1116b-106">A **New-AzureRmDnsZone** parancsmag egy új DNS-zónát hoz létre a megadott erőforráscsoport-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="1116b-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="1116b-107">Adjon meg egy egyedi DNS-zóna nevét a *Name* paraméterhez, vagy a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1116b-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="1116b-108">A zóna létrehozása után a New-AzureRmDnsRecordSet parancsmagot használva hozhat létre rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="1116b-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="1116b-109">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1116b-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1116b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1116b-110">EXAMPLES</span></span>

### <span data-ttu-id="1116b-111">Példa 1: DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="1116b-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1116b-112">Ez a parancs létrehoz egy új DNS-zónát a megadott erőforráscsoport myzone.com, majd a $Zone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1116b-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="1116b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1116b-113">PARAMETERS</span></span>

### <span data-ttu-id="1116b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1116b-114">-Name</span></span>
<span data-ttu-id="1116b-115">A létrehozandó DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1116b-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1116b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1116b-116">-ResourceGroupName</span></span>
<span data-ttu-id="1116b-117">Azt az erőforráscsoportot adja meg, amelybe a zónát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="1116b-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1116b-118">-Címke</span><span class="sxs-lookup"><span data-stu-id="1116b-118">-Tag</span></span>
<span data-ttu-id="1116b-119">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="1116b-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1116b-120">Példa:</span><span class="sxs-lookup"><span data-stu-id="1116b-120">For example:</span></span>

<span data-ttu-id="1116b-121">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="1116b-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1116b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1116b-122">-Confirm</span></span>
<span data-ttu-id="1116b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1116b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1116b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1116b-124">-WhatIf</span></span>
<span data-ttu-id="1116b-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1116b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1116b-126">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1116b-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1116b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1116b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1116b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1116b-128">-DefaultProfile</span></span>
<span data-ttu-id="1116b-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1116b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1116b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1116b-130">CommonParameters</span></span>
<span data-ttu-id="1116b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1116b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1116b-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1116b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1116b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1116b-133">INPUTS</span></span>

### <span data-ttu-id="1116b-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="1116b-134">None</span></span>
<span data-ttu-id="1116b-135">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="1116b-135">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="1116b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1116b-136">OUTPUTS</span></span>

### <span data-ttu-id="1116b-137">Microsoft. Azure. Command. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="1116b-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="1116b-138">Ez a parancsmag az új DNS-zónát képviselő Microsoft. Azure. Command. DNS. DnsZone objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="1116b-138">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="1116b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1116b-139">NOTES</span></span>
<span data-ttu-id="1116b-140">A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1116b-140">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1116b-141">A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.</span><span class="sxs-lookup"><span data-stu-id="1116b-141">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="1116b-142">Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1116b-142">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1116b-143">Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1116b-143">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1116b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1116b-144">RELATED LINKS</span></span>

[<span data-ttu-id="1116b-145">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1116b-145">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="1116b-146">Új – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1116b-146">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="1116b-147">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="1116b-147">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
