---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 2836445eabc4b3986a548adf7013ceaa7e75dc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500148"
---
# <span data-ttu-id="c87a1-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="c87a1-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="c87a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c87a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c87a1-103">Alapértelmezett érték beállítása az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="c87a1-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c87a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c87a1-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c87a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c87a1-106">Az Set-AzureRmDefault parancsmag az aktuális környezetben az alapértelmezett beállításokat adja meg vagy módosítja.</span><span class="sxs-lookup"><span data-stu-id="c87a1-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="c87a1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c87a1-107">EXAMPLES</span></span>

### <span data-ttu-id="c87a1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c87a1-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="c87a1-109">Ez a parancs beállítja az alapértelmezett erőforrás csoportot a felhasználó által megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="c87a1-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="c87a1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c87a1-110">PARAMETERS</span></span>

### <span data-ttu-id="c87a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87a1-111">-DefaultProfile</span></span>
<span data-ttu-id="c87a1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c87a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c87a1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c87a1-113">-Force</span></span>
<span data-ttu-id="c87a1-114">Új erőforráscsoport létrehozása, ha a megadott alapértelmezett érték nem létezik</span><span class="sxs-lookup"><span data-stu-id="c87a1-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="c87a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c87a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="c87a1-116">Az alapértelmezettként beállított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c87a1-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87a1-117">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="c87a1-117">-Scope</span></span>
<span data-ttu-id="c87a1-118">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="c87a1-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c87a1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c87a1-119">-Confirm</span></span>
<span data-ttu-id="c87a1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c87a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87a1-121">-WhatIf</span></span>
<span data-ttu-id="c87a1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c87a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87a1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c87a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87a1-124">CommonParameters</span></span>
<span data-ttu-id="c87a1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c87a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87a1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87a1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87a1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c87a1-127">INPUTS</span></span>

### <span data-ttu-id="c87a1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c87a1-128">System.String</span></span>

## <span data-ttu-id="c87a1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c87a1-129">OUTPUTS</span></span>

### <span data-ttu-id="c87a1-130">Microsoft. Azure. Command. profil. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c87a1-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="c87a1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c87a1-131">NOTES</span></span>

## <span data-ttu-id="c87a1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c87a1-132">RELATED LINKS</span></span>
