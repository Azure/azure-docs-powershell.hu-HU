---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160699"
---
# <span data-ttu-id="afbbc-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbbc-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="afbbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="afbbc-103">Nyilvános IP-cím eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="afbbc-103">Removes a public IP address.</span></span>

## <span data-ttu-id="afbbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="afbbc-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afbbc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="afbbc-105">DESCRIPTION</span></span>
<span data-ttu-id="afbbc-106">A **Remove-AzPublicIpAddress** parancsmag eltávolítja az Azure nyilvános IP-címét.</span><span class="sxs-lookup"><span data-stu-id="afbbc-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="afbbc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="afbbc-107">EXAMPLES</span></span>

### <span data-ttu-id="afbbc-108">1: Nyilvános IP-cím típusú erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="afbbc-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="afbbc-109">Ez a parancs eltávolítja a nyilvános IP-cím $publicIpName az erőforráscsoportban $rgName.</span><span class="sxs-lookup"><span data-stu-id="afbbc-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="afbbc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afbbc-110">PARAMETERS</span></span>

### <span data-ttu-id="afbbc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afbbc-111">-AsJob</span></span>
<span data-ttu-id="afbbc-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="afbbc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afbbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbbc-113">-DefaultProfile</span></span>
<span data-ttu-id="afbbc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afbbc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afbbc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="afbbc-115">-Force</span></span>
<span data-ttu-id="afbbc-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="afbbc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afbbc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="afbbc-117">-Name</span></span>
<span data-ttu-id="afbbc-118">A parancsmag által eltávolított nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="afbbc-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="afbbc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afbbc-119">-PassThru</span></span>
<span data-ttu-id="afbbc-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="afbbc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="afbbc-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="afbbc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="afbbc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afbbc-122">-ResourceGroupName</span></span>
<span data-ttu-id="afbbc-123">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által eltávolított nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="afbbc-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="afbbc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afbbc-124">-Confirm</span></span>
<span data-ttu-id="afbbc-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="afbbc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afbbc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afbbc-126">-WhatIf</span></span>
<span data-ttu-id="afbbc-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="afbbc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afbbc-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="afbbc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afbbc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbbc-129">CommonParameters</span></span>
<span data-ttu-id="afbbc-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afbbc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbbc-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afbbc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbbc-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afbbc-132">INPUTS</span></span>

### <span data-ttu-id="afbbc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="afbbc-133">System.String</span></span>

## <span data-ttu-id="afbbc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afbbc-134">OUTPUTS</span></span>

### <span data-ttu-id="afbbc-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afbbc-135">System.Boolean</span></span>

## <span data-ttu-id="afbbc-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="afbbc-136">NOTES</span></span>

## <span data-ttu-id="afbbc-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afbbc-137">RELATED LINKS</span></span>

[<span data-ttu-id="afbbc-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbbc-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="afbbc-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbbc-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="afbbc-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbbc-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


