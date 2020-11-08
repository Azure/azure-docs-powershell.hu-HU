---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194259"
---
# <span data-ttu-id="91e6c-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91e6c-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="91e6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="91e6c-103">CustomIpPrefix-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="91e6c-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="91e6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91e6c-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91e6c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="91e6c-106">A **New-AzCustomIpPrefix** parancsmag létrehoz egy CustomIpPrefix-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="91e6c-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="91e6c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="91e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="91e6c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91e6c-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="91e6c-109">Ez a parancs létrehoz egy új CustomIpPrefix-erőforrást, amelynek neve $prefixName az erőforráscsoport $rgName a 40.40.40.0/24 westus</span><span class="sxs-lookup"><span data-stu-id="91e6c-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="91e6c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="91e6c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91e6c-111">-AsJob</span></span>
<span data-ttu-id="91e6c-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="91e6c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91e6c-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="91e6c-113">-Cidr</span></span>
<span data-ttu-id="91e6c-114">A CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="91e6c-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e6c-115">-DefaultProfile</span></span>
<span data-ttu-id="91e6c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91e6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="91e6c-117">-Location</span></span>
<span data-ttu-id="91e6c-118">A CustomIpPrefix helye.</span><span class="sxs-lookup"><span data-stu-id="91e6c-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91e6c-119">-Name</span></span>
<span data-ttu-id="91e6c-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="91e6c-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="91e6c-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="91e6c-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="91e6c-123">-Tag</span></span>
<span data-ttu-id="91e6c-124">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="91e6c-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-125">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="91e6c-125">-Zone</span></span>
<span data-ttu-id="91e6c-126">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="91e6c-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91e6c-127">-Confirm</span></span>
<span data-ttu-id="91e6c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91e6c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e6c-129">-WhatIf</span></span>
<span data-ttu-id="91e6c-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91e6c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91e6c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91e6c-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e6c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e6c-132">CommonParameters</span></span>
<span data-ttu-id="91e6c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91e6c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e6c-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91e6c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e6c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91e6c-135">INPUTS</span></span>

### <span data-ttu-id="91e6c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="91e6c-136">System.String</span></span>

### <span data-ttu-id="91e6c-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="91e6c-137">System.String[]</span></span>

### <span data-ttu-id="91e6c-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="91e6c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="91e6c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91e6c-139">OUTPUTS</span></span>

### <span data-ttu-id="91e6c-140">Microsoft. Azure. commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91e6c-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="91e6c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91e6c-141">NOTES</span></span>

## <span data-ttu-id="91e6c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91e6c-142">RELATED LINKS</span></span>

[<span data-ttu-id="91e6c-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91e6c-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="91e6c-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91e6c-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="91e6c-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91e6c-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)