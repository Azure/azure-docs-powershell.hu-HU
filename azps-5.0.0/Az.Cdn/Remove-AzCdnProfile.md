---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187650"
---
# <span data-ttu-id="a9826-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9826-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="a9826-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9826-102">SYNOPSIS</span></span>
<span data-ttu-id="a9826-103">Egy CDN-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a9826-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="a9826-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9826-104">SYNTAX</span></span>

### <span data-ttu-id="a9826-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9826-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9826-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9826-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9826-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9826-107">DESCRIPTION</span></span>
<span data-ttu-id="a9826-108">A **Remove-AzCdnProfile** parancsmag eltávolítja az Azure Content Delivery Network (CDN) profilt.</span><span class="sxs-lookup"><span data-stu-id="a9826-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="a9826-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a9826-109">EXAMPLES</span></span>

## <span data-ttu-id="a9826-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9826-110">PARAMETERS</span></span>

### <span data-ttu-id="a9826-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9826-111">-CdnProfile</span></span>
<span data-ttu-id="a9826-112">A parancsmag által eltávolított profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9826-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a9826-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9826-113">-DefaultProfile</span></span>
<span data-ttu-id="a9826-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a9826-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9826-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a9826-115">-Force</span></span>
<span data-ttu-id="a9826-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a9826-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9826-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9826-117">-PassThru</span></span>
<span data-ttu-id="a9826-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a9826-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a9826-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a9826-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9826-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="a9826-120">-ProfileName</span></span>
<span data-ttu-id="a9826-121">Annak a profilnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="a9826-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a9826-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9826-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9826-123">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="a9826-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="a9826-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9826-124">-Confirm</span></span>
<span data-ttu-id="a9826-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9826-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9826-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9826-126">-WhatIf</span></span>
<span data-ttu-id="a9826-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9826-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9826-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9826-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9826-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9826-129">CommonParameters</span></span>
<span data-ttu-id="a9826-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9826-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9826-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a9826-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9826-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9826-132">INPUTS</span></span>

### <span data-ttu-id="a9826-133">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a9826-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="a9826-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9826-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9826-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9826-135">OUTPUTS</span></span>

### <span data-ttu-id="a9826-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9826-136">System.Boolean</span></span>

## <span data-ttu-id="a9826-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9826-137">NOTES</span></span>

## <span data-ttu-id="a9826-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9826-138">RELATED LINKS</span></span>

[<span data-ttu-id="a9826-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9826-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="a9826-140">Új – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9826-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="a9826-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9826-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


