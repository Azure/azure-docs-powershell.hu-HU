---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: a29bf86b4104fb9a3936daad055da0eab4368690
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680314"
---
# <span data-ttu-id="ba627-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="ba627-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="ba627-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba627-102">SYNOPSIS</span></span>
<span data-ttu-id="ba627-103">Törli a felhasználó által az aktuális környezetben beállított alapértékeket.</span><span class="sxs-lookup"><span data-stu-id="ba627-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba627-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba627-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba627-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba627-105">DESCRIPTION</span></span>
<span data-ttu-id="ba627-106">A Clear-AzureRmDefault parancsmag a felhasználó által megadott kapcsoló paramétertől függően eltávolítja a felhasználó által megadott alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="ba627-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="ba627-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba627-107">EXAMPLES</span></span>

### <span data-ttu-id="ba627-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ba627-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="ba627-109">Ez a parancs eltávolítja a felhasználó által az aktuális környezetben beállított összes alapértelmezett beállítást.</span><span class="sxs-lookup"><span data-stu-id="ba627-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="ba627-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ba627-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="ba627-111">Ez a parancs eltávolítja a felhasználó által az aktuális környezetben beállított alapértelmezett erőforráscsoport-csoportot.</span><span class="sxs-lookup"><span data-stu-id="ba627-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="ba627-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba627-112">PARAMETERS</span></span>

### <span data-ttu-id="ba627-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba627-113">-DefaultProfile</span></span>
<span data-ttu-id="ba627-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba627-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba627-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ba627-115">-Force</span></span>
<span data-ttu-id="ba627-116">Az összes alapértelmezett érték eltávolítása, ha nincs alapértelmezett megadva</span><span class="sxs-lookup"><span data-stu-id="ba627-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="ba627-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba627-117">-PassThru</span></span>
<span data-ttu-id="ba627-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ba627-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ba627-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba627-119">-ResourceGroup</span></span>
<span data-ttu-id="ba627-120">Az alapértelmezett erőforráscsoport törlése</span><span class="sxs-lookup"><span data-stu-id="ba627-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="ba627-121">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ba627-121">-Scope</span></span>
<span data-ttu-id="ba627-122">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="ba627-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba627-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba627-123">-Confirm</span></span>
<span data-ttu-id="ba627-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba627-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba627-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba627-125">-WhatIf</span></span>
<span data-ttu-id="ba627-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba627-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba627-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba627-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba627-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba627-128">CommonParameters</span></span>
<span data-ttu-id="ba627-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba627-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba627-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba627-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba627-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba627-131">INPUTS</span></span>

### <span data-ttu-id="ba627-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba627-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ba627-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba627-133">OUTPUTS</span></span>

### <span data-ttu-id="ba627-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba627-134">System.Boolean</span></span>

## <span data-ttu-id="ba627-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba627-135">NOTES</span></span>

## <span data-ttu-id="ba627-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba627-136">RELATED LINKS</span></span>
