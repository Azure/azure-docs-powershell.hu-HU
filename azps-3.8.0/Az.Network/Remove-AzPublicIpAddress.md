---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014004"
---
# <span data-ttu-id="23622-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="23622-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="23622-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23622-102">SYNOPSIS</span></span>
<span data-ttu-id="23622-103">Nyilvános IP-cím eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="23622-103">Removes a public IP address.</span></span>

## <span data-ttu-id="23622-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23622-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23622-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23622-105">DESCRIPTION</span></span>
<span data-ttu-id="23622-106">A **Remove-AzPublicIpAddress** parancsmag eltávolítja az Azure-alapú nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="23622-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="23622-107">Példák</span><span class="sxs-lookup"><span data-stu-id="23622-107">EXAMPLES</span></span>

### <span data-ttu-id="23622-108">1: nyilvános IP-cím erőforrásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="23622-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="23622-109">Ez a parancs eltávolítja a $publicIpName nevű nyilvános IP-cím erőforrást az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="23622-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="23622-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23622-110">PARAMETERS</span></span>

### <span data-ttu-id="23622-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23622-111">-AsJob</span></span>
<span data-ttu-id="23622-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="23622-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23622-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23622-113">-DefaultProfile</span></span>
<span data-ttu-id="23622-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23622-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23622-115">-Force</span><span class="sxs-lookup"><span data-stu-id="23622-115">-Force</span></span>
<span data-ttu-id="23622-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="23622-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23622-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23622-117">-Name</span></span>
<span data-ttu-id="23622-118">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="23622-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="23622-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23622-119">-PassThru</span></span>
<span data-ttu-id="23622-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="23622-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="23622-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="23622-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23622-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23622-122">-ResourceGroupName</span></span>
<span data-ttu-id="23622-123">Annak a csoportnak a neve, amely a parancsmag által eltávolított nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="23622-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="23622-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23622-124">-Confirm</span></span>
<span data-ttu-id="23622-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23622-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23622-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23622-126">-WhatIf</span></span>
<span data-ttu-id="23622-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23622-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23622-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23622-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23622-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23622-129">CommonParameters</span></span>
<span data-ttu-id="23622-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23622-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23622-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23622-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23622-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23622-132">INPUTS</span></span>

### <span data-ttu-id="23622-133">System. String</span><span class="sxs-lookup"><span data-stu-id="23622-133">System.String</span></span>

## <span data-ttu-id="23622-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23622-134">OUTPUTS</span></span>

### <span data-ttu-id="23622-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23622-135">System.Boolean</span></span>

## <span data-ttu-id="23622-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23622-136">NOTES</span></span>

## <span data-ttu-id="23622-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23622-137">RELATED LINKS</span></span>

[<span data-ttu-id="23622-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="23622-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="23622-139">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="23622-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="23622-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="23622-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


