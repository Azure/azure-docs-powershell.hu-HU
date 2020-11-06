---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 6d294bd4b6f016ed1731a71528b39adc3bbe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503519"
---
# <span data-ttu-id="97050-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="97050-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="97050-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97050-102">SYNOPSIS</span></span>
<span data-ttu-id="97050-103">Nyilvános IP-cím eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="97050-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97050-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97050-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97050-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97050-105">DESCRIPTION</span></span>
<span data-ttu-id="97050-106">A **Remove-AzureRmPublicIpAddress** parancsmag eltávolítja az Azure-alapú nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="97050-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="97050-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97050-107">EXAMPLES</span></span>

### <span data-ttu-id="97050-108">1: nyilvános IP-cím erőforrásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="97050-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="97050-109">Ez a parancs eltávolítja a $publicIpName nevű nyilvános IP-cím erőforrást az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="97050-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="97050-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97050-110">PARAMETERS</span></span>

### <span data-ttu-id="97050-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97050-111">-AsJob</span></span>
<span data-ttu-id="97050-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="97050-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97050-113">-DefaultProfile</span></span>
<span data-ttu-id="97050-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97050-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97050-115">-Force</span><span class="sxs-lookup"><span data-stu-id="97050-115">-Force</span></span>
<span data-ttu-id="97050-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="97050-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97050-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97050-117">-Name</span></span>
<span data-ttu-id="97050-118">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="97050-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97050-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97050-119">-PassThru</span></span>
<span data-ttu-id="97050-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="97050-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97050-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="97050-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97050-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97050-122">-ResourceGroupName</span></span>
<span data-ttu-id="97050-123">Annak a csoportnak a neve, amely a parancsmag által eltávolított nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="97050-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="97050-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97050-124">-Confirm</span></span>
<span data-ttu-id="97050-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97050-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97050-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97050-126">-WhatIf</span></span>
<span data-ttu-id="97050-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97050-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97050-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97050-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97050-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97050-129">CommonParameters</span></span>
<span data-ttu-id="97050-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97050-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97050-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97050-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97050-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97050-132">INPUTS</span></span>

### <span data-ttu-id="97050-133">System. String</span><span class="sxs-lookup"><span data-stu-id="97050-133">System.String</span></span>

## <span data-ttu-id="97050-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97050-134">OUTPUTS</span></span>

### <span data-ttu-id="97050-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97050-135">System.Boolean</span></span>

## <span data-ttu-id="97050-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97050-136">NOTES</span></span>

## <span data-ttu-id="97050-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97050-137">RELATED LINKS</span></span>

[<span data-ttu-id="97050-138">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="97050-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="97050-139">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="97050-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="97050-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="97050-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


