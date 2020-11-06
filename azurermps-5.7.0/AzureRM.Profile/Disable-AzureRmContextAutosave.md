---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 622cbd399f554173bbe9734429f4ae787fe94d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492235"
---
# <span data-ttu-id="9f6f6-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="9f6f6-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="9f6f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6f6-103">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="9f6f6-104">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="9f6f6-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f6f6-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f6f6-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6f6-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f6f6-106">DESCRIPTION</span></span>
<span data-ttu-id="9f6f6-107">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="9f6f6-108">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="9f6f6-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="9f6f6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9f6f6-109">EXAMPLES</span></span>

### <span data-ttu-id="9f6f6-110">A környezet automatikus mentésének letiltása</span><span class="sxs-lookup"><span data-stu-id="9f6f6-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="9f6f6-111">Tiltsa le az automatikus mentés funkciót az aktuális felhasználónál.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="9f6f6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f6f6-112">PARAMETERS</span></span>

### <span data-ttu-id="9f6f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6f6-113">-DefaultProfile</span></span>
<span data-ttu-id="9f6f6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f6f6-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f6f6-115">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="9f6f6-115">-Scope</span></span>
<span data-ttu-id="9f6f6-116">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6f6-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f6f6-117">-Confirm</span></span>
<span data-ttu-id="9f6f6-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6f6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6f6-119">-WhatIf</span></span>
<span data-ttu-id="9f6f6-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6f6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6f6-122">CommonParameters</span></span>
<span data-ttu-id="9f6f6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f6f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6f6-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6f6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6f6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f6f6-125">INPUTS</span></span>

### <span data-ttu-id="9f6f6-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="9f6f6-126">None</span></span>

## <span data-ttu-id="9f6f6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f6f6-127">OUTPUTS</span></span>

### <span data-ttu-id="9f6f6-128">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="9f6f6-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="9f6f6-129">A jelenlegi automatikus mentés beállításairól szóló információk, például hogy engedélyezve van-e az automatikus mentés az aktuális felhasználó számára, és hogy hol vannak mentve a környezet és a hitelesítőadat-fájlok.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="9f6f6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f6f6-130">NOTES</span></span>

## <span data-ttu-id="9f6f6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f6f6-131">RELATED LINKS</span></span>

