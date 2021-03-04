---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 904af1f1d1f6cba7bd0a44ee0811b55fef01e106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941961"
---
# <span data-ttu-id="79075-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79075-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="79075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79075-102">SYNOPSIS</span></span>
<span data-ttu-id="79075-103">Eltávolít egy CDN-profilt.</span><span class="sxs-lookup"><span data-stu-id="79075-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="79075-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79075-104">SYNTAX</span></span>

### <span data-ttu-id="79075-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="79075-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79075-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79075-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79075-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79075-107">DESCRIPTION</span></span>
<span data-ttu-id="79075-108">A **Remove-AzCdnProfile** parancsmag eltávolítja az Azure Content Delivery Network (CDN) profilt.</span><span class="sxs-lookup"><span data-stu-id="79075-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="79075-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79075-109">EXAMPLES</span></span>

## <span data-ttu-id="79075-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79075-110">PARAMETERS</span></span>

### <span data-ttu-id="79075-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="79075-111">-CdnProfile</span></span>
<span data-ttu-id="79075-112">Azt a profilt adja meg, amelyből a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="79075-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="79075-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79075-113">-DefaultProfile</span></span>
<span data-ttu-id="79075-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79075-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79075-115">-Force</span><span class="sxs-lookup"><span data-stu-id="79075-115">-Force</span></span>
<span data-ttu-id="79075-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="79075-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79075-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79075-117">-PassThru</span></span>
<span data-ttu-id="79075-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="79075-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="79075-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="79075-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="79075-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="79075-120">-ProfileName</span></span>
<span data-ttu-id="79075-121">Annak a profilnak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="79075-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="79075-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79075-122">-ResourceGroupName</span></span>
<span data-ttu-id="79075-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="79075-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="79075-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79075-124">-Confirm</span></span>
<span data-ttu-id="79075-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79075-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79075-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79075-126">-WhatIf</span></span>
<span data-ttu-id="79075-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79075-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79075-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79075-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79075-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79075-129">CommonParameters</span></span>
<span data-ttu-id="79075-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79075-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79075-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79075-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79075-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79075-132">INPUTS</span></span>

### <span data-ttu-id="79075-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="79075-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="79075-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79075-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79075-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79075-135">OUTPUTS</span></span>

### <span data-ttu-id="79075-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79075-136">System.Boolean</span></span>

## <span data-ttu-id="79075-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79075-137">NOTES</span></span>

## <span data-ttu-id="79075-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79075-138">RELATED LINKS</span></span>

[<span data-ttu-id="79075-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79075-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="79075-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79075-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="79075-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79075-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


