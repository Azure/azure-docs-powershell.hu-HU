---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343805"
---
# <span data-ttu-id="54be7-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="54be7-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="54be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54be7-102">SYNOPSIS</span></span>
<span data-ttu-id="54be7-103">Létrehoz egy új privát DNS-zónát.</span><span class="sxs-lookup"><span data-stu-id="54be7-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="54be7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="54be7-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54be7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="54be7-105">DESCRIPTION</span></span>
<span data-ttu-id="54be7-106">A **New-AzPrivateDnsZone** parancsmag létrehoz egy új dns-zónát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="54be7-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="54be7-107">A Name paraméterhez egyedi privát  DNS-zónanevet kell megadnia, különben a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="54be7-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="54be7-108">A zóna létrehozása után a New-AzPrivateDnsRecordSet parancsmag használatával hozzon létre rekordkészleteket a zónában.</span><span class="sxs-lookup"><span data-stu-id="54be7-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="54be7-109">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="54be7-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="54be7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="54be7-110">EXAMPLES</span></span>

### <span data-ttu-id="54be7-111">1. példa: Privát DNS-zóna létrehozása</span><span class="sxs-lookup"><span data-stu-id="54be7-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="54be7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54be7-112">PARAMETERS</span></span>

### <span data-ttu-id="54be7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54be7-113">-DefaultProfile</span></span>
<span data-ttu-id="54be7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="54be7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54be7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="54be7-115">-Name</span></span>
<span data-ttu-id="54be7-116">A létrehozni szükséges privát DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="54be7-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="54be7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54be7-117">-ResourceGroupName</span></span>
<span data-ttu-id="54be7-118">Megadja azt az erőforráscsoportot, amelyben létre kell hoznia a zónát.</span><span class="sxs-lookup"><span data-stu-id="54be7-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="54be7-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="54be7-119">-Tag</span></span>
<span data-ttu-id="54be7-120">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="54be7-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="54be7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54be7-121">-Confirm</span></span>
<span data-ttu-id="54be7-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="54be7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54be7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54be7-123">-WhatIf</span></span>
<span data-ttu-id="54be7-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="54be7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54be7-125">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="54be7-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54be7-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54be7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54be7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54be7-127">CommonParameters</span></span>
<span data-ttu-id="54be7-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54be7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54be7-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54be7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54be7-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54be7-130">INPUTS</span></span>

### <span data-ttu-id="54be7-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="54be7-131">None</span></span>

## <span data-ttu-id="54be7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54be7-132">OUTPUTS</span></span>

### <span data-ttu-id="54be7-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="54be7-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="54be7-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="54be7-134">NOTES</span></span>

## <span data-ttu-id="54be7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54be7-135">RELATED LINKS</span></span>

[<span data-ttu-id="54be7-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="54be7-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="54be7-137">Új-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="54be7-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="54be7-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="54be7-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
