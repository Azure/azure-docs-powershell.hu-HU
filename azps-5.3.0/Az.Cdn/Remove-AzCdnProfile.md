---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477974"
---
# <span data-ttu-id="90541-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90541-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="90541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90541-102">SYNOPSIS</span></span>
<span data-ttu-id="90541-103">Eltávolít egy CDN-profilt.</span><span class="sxs-lookup"><span data-stu-id="90541-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="90541-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90541-104">SYNTAX</span></span>

### <span data-ttu-id="90541-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="90541-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90541-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90541-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90541-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90541-107">DESCRIPTION</span></span>
<span data-ttu-id="90541-108">A **Remove-AzCdnProfile** parancsmag eltávolítja az Azure Content Delivery Network (CDN) profilt.</span><span class="sxs-lookup"><span data-stu-id="90541-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="90541-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90541-109">EXAMPLES</span></span>

## <span data-ttu-id="90541-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90541-110">PARAMETERS</span></span>

### <span data-ttu-id="90541-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="90541-111">-CdnProfile</span></span>
<span data-ttu-id="90541-112">Azt a profilt adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="90541-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90541-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90541-113">-DefaultProfile</span></span>
<span data-ttu-id="90541-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="90541-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90541-115">-Force</span><span class="sxs-lookup"><span data-stu-id="90541-115">-Force</span></span>
<span data-ttu-id="90541-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="90541-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="90541-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90541-117">-PassThru</span></span>
<span data-ttu-id="90541-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="90541-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="90541-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="90541-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90541-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="90541-120">-ProfileName</span></span>
<span data-ttu-id="90541-121">Annak a profilnak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="90541-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90541-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90541-122">-ResourceGroupName</span></span>
<span data-ttu-id="90541-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="90541-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90541-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90541-124">-Confirm</span></span>
<span data-ttu-id="90541-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90541-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90541-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90541-126">-WhatIf</span></span>
<span data-ttu-id="90541-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="90541-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90541-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90541-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90541-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90541-129">CommonParameters</span></span>
<span data-ttu-id="90541-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90541-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90541-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90541-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90541-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90541-132">INPUTS</span></span>

### <span data-ttu-id="90541-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="90541-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="90541-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90541-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90541-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90541-135">OUTPUTS</span></span>

### <span data-ttu-id="90541-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90541-136">System.Boolean</span></span>

## <span data-ttu-id="90541-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90541-137">NOTES</span></span>

## <span data-ttu-id="90541-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90541-138">RELATED LINKS</span></span>

[<span data-ttu-id="90541-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90541-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="90541-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90541-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="90541-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90541-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


