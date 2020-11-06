---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497867"
---
# <span data-ttu-id="e9951-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="e9951-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9951-102">SYNOPSIS</span></span>
<span data-ttu-id="e9951-103">Egy CDN-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e9951-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9951-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9951-104">SYNTAX</span></span>

### <span data-ttu-id="e9951-105">A mezők paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="e9951-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9951-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="e9951-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9951-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9951-107">DESCRIPTION</span></span>
<span data-ttu-id="e9951-108">A **Remove-AzureRmCdnProfile** parancsmag eltávolítja az Azure Content Delivery Network (CDN) profilt.</span><span class="sxs-lookup"><span data-stu-id="e9951-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="e9951-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e9951-109">EXAMPLES</span></span>

## <span data-ttu-id="e9951-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9951-110">PARAMETERS</span></span>

### <span data-ttu-id="e9951-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-111">-CdnProfile</span></span>
<span data-ttu-id="e9951-112">A parancsmag által eltávolított profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9951-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9951-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e9951-113">-Force</span></span>
<span data-ttu-id="e9951-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e9951-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e9951-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9951-115">-PassThru</span></span>
<span data-ttu-id="e9951-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e9951-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e9951-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e9951-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9951-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="e9951-118">-ProfileName</span></span>
<span data-ttu-id="e9951-119">Annak a profilnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e9951-119">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9951-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9951-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9951-121">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="e9951-121">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9951-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e9951-122">-Confirm</span></span>
<span data-ttu-id="e9951-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9951-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9951-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9951-124">-WhatIf</span></span>
<span data-ttu-id="e9951-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e9951-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9951-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9951-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9951-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-127">-DefaultProfile</span></span>
<span data-ttu-id="e9951-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9951-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9951-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9951-129">CommonParameters</span></span>
<span data-ttu-id="e9951-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9951-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9951-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9951-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9951-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9951-132">INPUTS</span></span>

### <span data-ttu-id="e9951-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-133">PSProfile</span></span>
<span data-ttu-id="e9951-134">A ' CdnProfile ' paraméter az "PSProfile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e9951-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="e9951-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9951-135">OUTPUTS</span></span>

### <span data-ttu-id="e9951-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9951-136">System.Boolean</span></span>

## <span data-ttu-id="e9951-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9951-137">NOTES</span></span>

## <span data-ttu-id="e9951-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9951-138">RELATED LINKS</span></span>

[<span data-ttu-id="e9951-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="e9951-140">Új – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="e9951-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


