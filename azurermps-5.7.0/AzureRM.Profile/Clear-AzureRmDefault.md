---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492237"
---
# <span data-ttu-id="0fd5c-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="0fd5c-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="0fd5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd5c-103">Törli a felhasználó által az aktuális környezetben beállított alapértékeket.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fd5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fd5c-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fd5c-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd5c-106">A Clear-AzureRmDefault parancsmag a felhasználó által megadott kapcsoló paramétertől függően eltávolítja a felhasználó által megadott alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="0fd5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0fd5c-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd5c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fd5c-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="0fd5c-109">Ez a parancs eltávolítja a felhasználó által az aktuális környezetben beállított összes alapértelmezett beállítást.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="0fd5c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fd5c-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="0fd5c-111">Ez a parancs eltávolítja a felhasználó által az aktuális környezetben beállított alapértelmezett erőforráscsoport-csoportot.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="0fd5c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fd5c-112">PARAMETERS</span></span>

### <span data-ttu-id="0fd5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd5c-113">-DefaultProfile</span></span>
<span data-ttu-id="0fd5c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd5c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0fd5c-115">-Force</span></span>
<span data-ttu-id="0fd5c-116">Az összes alapértelmezett érték eltávolítása, ha nincs alapértelmezett megadva</span><span class="sxs-lookup"><span data-stu-id="0fd5c-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="0fd5c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fd5c-117">-PassThru</span></span>
<span data-ttu-id="0fd5c-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0fd5c-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0fd5c-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0fd5c-119">-ResourceGroup</span></span>
<span data-ttu-id="0fd5c-120">Az alapértelmezett erőforráscsoport törlése</span><span class="sxs-lookup"><span data-stu-id="0fd5c-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd5c-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fd5c-121">-Confirm</span></span>
<span data-ttu-id="0fd5c-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd5c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd5c-123">-WhatIf</span></span>
<span data-ttu-id="0fd5c-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd5c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd5c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd5c-126">CommonParameters</span></span>
<span data-ttu-id="0fd5c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fd5c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd5c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd5c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd5c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fd5c-129">INPUTS</span></span>

### <span data-ttu-id="0fd5c-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0fd5c-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0fd5c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fd5c-131">OUTPUTS</span></span>

### <span data-ttu-id="0fd5c-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="0fd5c-132">System.Object</span></span>

## <span data-ttu-id="0fd5c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fd5c-133">NOTES</span></span>

## <span data-ttu-id="0fd5c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fd5c-134">RELATED LINKS</span></span>

