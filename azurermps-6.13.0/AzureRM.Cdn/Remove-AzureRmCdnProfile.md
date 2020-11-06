---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498371"
---
# <span data-ttu-id="a5cf6-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf6-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="a5cf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cf6-103">Egy CDN-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5cf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5cf6-104">SYNTAX</span></span>

### <span data-ttu-id="a5cf6-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5cf6-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5cf6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5cf6-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5cf6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="a5cf6-108">A **Remove-AzureRmCdnProfile** parancsmag eltávolítja az Azure Content Delivery Network (CDN) profilt.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="a5cf6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a5cf6-109">EXAMPLES</span></span>

## <span data-ttu-id="a5cf6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5cf6-110">PARAMETERS</span></span>

### <span data-ttu-id="a5cf6-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf6-111">-CdnProfile</span></span>
<span data-ttu-id="a5cf6-112">A parancsmag által eltávolított profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a5cf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf6-113">-DefaultProfile</span></span>
<span data-ttu-id="a5cf6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5cf6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5cf6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5cf6-115">-Force</span></span>
<span data-ttu-id="a5cf6-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5cf6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5cf6-117">-PassThru</span></span>
<span data-ttu-id="a5cf6-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5cf6-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5cf6-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="a5cf6-120">-ProfileName</span></span>
<span data-ttu-id="a5cf6-121">Annak a profilnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a5cf6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cf6-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5cf6-123">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="a5cf6-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5cf6-124">-Confirm</span></span>
<span data-ttu-id="a5cf6-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5cf6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5cf6-126">-WhatIf</span></span>
<span data-ttu-id="a5cf6-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5cf6-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5cf6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cf6-129">CommonParameters</span></span>
<span data-ttu-id="a5cf6-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5cf6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cf6-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5cf6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cf6-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5cf6-132">INPUTS</span></span>

### <span data-ttu-id="a5cf6-133">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf6-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="a5cf6-134">Paraméterek: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5cf6-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="a5cf6-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5cf6-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a5cf6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5cf6-136">OUTPUTS</span></span>

### <span data-ttu-id="a5cf6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5cf6-137">System.Boolean</span></span>

## <span data-ttu-id="a5cf6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5cf6-138">NOTES</span></span>

## <span data-ttu-id="a5cf6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5cf6-139">RELATED LINKS</span></span>

[<span data-ttu-id="a5cf6-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf6-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="a5cf6-141">Új – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf6-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="a5cf6-142">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf6-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


