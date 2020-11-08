---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184708"
---
# <span data-ttu-id="cb5a4-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cb5a4-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="cb5a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5a4-103">Új magánhálózati DNS-zónát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="cb5a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb5a4-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb5a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5a4-106">A **New-AzPrivateDnsZone** parancsmag egy új, privát tartománynévrendszer (DNS) zónát hoz létre a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="cb5a4-107">Adjon meg egy egyedi magánhálózati DNS-zóna nevét a *Name (név* ) paraméterhez, vagy a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="cb5a4-108">A zóna létrehozása után a New-AzPrivateDnsRecordSet parancsmagot használva hozhat létre rekordokat a zónában.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="cb5a4-109">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="cb5a4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cb5a4-110">EXAMPLES</span></span>

### <span data-ttu-id="cb5a4-111">Példa 1: privát DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="cb5a4-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="cb5a4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb5a4-112">PARAMETERS</span></span>

### <span data-ttu-id="cb5a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5a4-113">-DefaultProfile</span></span>
<span data-ttu-id="cb5a4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cb5a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb5a4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb5a4-115">-Name</span></span>
<span data-ttu-id="cb5a4-116">A létrehozandó magánhálózati DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-116">Specifies the name of the private DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb5a4-118">Azt az erőforráscsoportot adja meg, amelybe a zónát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-118">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5a4-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="cb5a4-119">-Tag</span></span>
<span data-ttu-id="cb5a4-120">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5a4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb5a4-121">-Confirm</span></span>
<span data-ttu-id="cb5a4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb5a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb5a4-123">-WhatIf</span></span>
<span data-ttu-id="cb5a4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb5a4-125">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb5a4-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb5a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5a4-127">CommonParameters</span></span>
<span data-ttu-id="cb5a4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb5a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5a4-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5a4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb5a4-130">INPUTS</span></span>

### <span data-ttu-id="cb5a4-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="cb5a4-131">None</span></span>

## <span data-ttu-id="cb5a4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb5a4-132">OUTPUTS</span></span>

### <span data-ttu-id="cb5a4-133">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cb5a4-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="cb5a4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb5a4-134">NOTES</span></span>

## <span data-ttu-id="cb5a4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb5a4-135">RELATED LINKS</span></span>

[<span data-ttu-id="cb5a4-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cb5a4-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="cb5a4-137">Új – AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cb5a4-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="cb5a4-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="cb5a4-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
